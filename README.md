# keycloak-with-vue-vuetify-theme
Keycloak themes using vue + vuetify

# Project Structure
- certs - A folder to map your certificates for the keycloak server
- keycloak-vue - The keycloak theme using vue + vuetify
- scripts - usefull scripts to run the keycloak server, like a script  to initialize postgres database using environment variables

# **How to run**
Change the volume paths in the docker-compose.yml file to your local paths, case you need.
## **Running in development mode**
Create a copy of the **.env.template** file and rename it to **.env**, then fill the variables with your values.

## **Running in production mode**
Create a copy of the **.env.template** file and rename it to **.env**, then fill the variables with your values.

We recommend setting the following variables, with the following values:
```bash
KEYCLOAK_DOCKER_COMMAND=--start --optimized
KEYCLOAK_DOCKER_BUILD_TARGET=production
KEYCLOAK_HTTP_PORT=80
KEYCLOAK_HTTPS_PORT=443
```
It's also recomend to uncomment the volumes under keycloak service definition and map with yours proper certificates

# **Developing theme**
You can use this project as a reference to create your own themes.

The theme is using vue + vuetify, so you can use all the components from vuetify. You can also use the components from the keycloak theme, like the login form, the register form, etc.

# How to copy keycloak themes

## Pre requisites
You must have the keycloak server running.

Case you are using vscode you can run it just pressing F5

IMPORTANT: You must open **keycloak-with-vue-vuetify-theme.code-workspace** as a workspace in VSCODE.

## **Copying themes**
To copy the themes to the keycloak server, you can use the script **scripts/copy-themes.sh**. Or you can run a vscode task that will start the container and copy it for you. 

We recomend you to copy the theme to a folder ignored by git, like **keycloak-base-themes**. This way you can keep your theme in a git repository and copy it to the keycloak server.

The copied file can be opened using any standard ZIP archive tool.
