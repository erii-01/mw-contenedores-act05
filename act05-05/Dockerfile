FROM redmine:5

# Cambiar al usuario root temporalmente
USER root

# Instalar 'git'
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

# Ir al directorio de plugins de Redmine
WORKDIR /usr/src/redmine/plugins

# Clonar el plugin desde su repositorio de GitHub
RUN git clone --branch 3.3.2 https://github.com/AlphaNodes/additionals.git

# Volver al directorio principal de Redmine para instalar las dependencias
WORKDIR /usr/src/redmine

# Instalar las 'gems' (dependencias de Ruby) que el plugin necesita
RUN bundle install --without development test

# Cambiar el propietario de los archivos al usuario 'redmine'
RUN chown -R redmine:redmine plugins/additionals

# Volver a ser el usuario 'redmine' para la ejecución normal
USER redmine