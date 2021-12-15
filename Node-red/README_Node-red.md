

## Introducción

En este README se va a explicar todo lo que se ha realizado en Node-red, explicando paso a paso todas las configuraciones y por otro lado, también se va a explicar la utilización de la herramienta tecnológica DOCKER.

## Instalaciones

Cabe destacar que hay varias vías para tener Node-red instalado: 
* **Localmente**: se puede instalar Node-red localmente siguiendo los siguentes pasos:
  - 1- Instalando Node js mediante la URL ---> (https://nodejs.org/es/).
  - 2- Ejecutando el comando 'npm install -g --unsafe-perm node-red' para instalar Node-red.
  - 3- Correr la aplicación - **in a terminal window** -> npm node-red.
  - 
| Command                    | Description                                                                                                 |
| -------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `npm run ng:serve:web`     | Execute the app in the browser                                                                              |
| `npm run build`            | Build the app. Your built files are in the /dist folder.                                                    |
| `npm run build:prod`       | Build the app with Angular aot. Your built files are in the /dist folder.                                   |
| `npm run electron:local`   | Builds your application and start electron                                                                  |
| `npm run electron:linux`   | Builds your application and creates an app consumable on linux system                                       |
| `npm run electron:windows` | On a Windows OS, builds your application and creates an app consumable in windows 32/64 bit systems         |
| `npm run electron:mac`     | On a MAC OS, builds your application and generates a `.app` file of your application that can be run on Mac |


* Views (https://www.drupal.org/project/views)
* Panels (https://www.drupal.org/project/panels)


## RECOMMENDED

* Markdown filter (https://www.drupal.org/project/markdown):
  When enabled, display of the project's README.md help will be rendered
  with markdown.


## INSTALLATION
 
* Install as you would normally install a contributed Drupal module. Visit
  https://www.drupal.org/documentation/install/modules-themes/modules-7 for
  further information.

* You may want to disable Toolbar module, since its output clashes with
  Administration Menu.


## CONFIGURATION
 
* Configure the user permissions in Administration » People » Permissions:

  - Use the administration pages and help (System module)

    The top-level administration categories require this permission to be
    accessible. The administration menu will be empty unless this permission
    is granted.

  - Access administration menu

    Users with this permission will see the administration menu at the top of
    each page.

  - Display Drupal links

    Users with this permission will receive links to drupal.org issue queues for
    all enabled contributed modules. The issue queue links appear under the
    administration menu icon.

* Customize the menu settings in Administration » Configuration and modules »
  Administration » Administration menu.

* To prevent administrative menu items from appearing twice, you may hide the
  "Management" menu block.


## CONFIGURATION

The module has no menu or modifiable settings. There is no configuration. When
enabled, the module will prevent the links from appearing. To get the links
back, disable the module and clear caches.


## TROUBLESHOOTING

* If the menu does not display, check the following:

  - Are the "Access administration menu" and "Use the administration pages and
    help" permissions enabled for the appropriate roles?

  - Does html.tpl.php of your theme output the $page_bottom variable?


## FAQ

Q: I enabled "Aggregate and compress CSS files", but admin_menu.css is still
   there. Is this normal?

A: Yes, this is the intended behavior. the administration menu module only loads
   its stylesheet as needed (i.e., on page requests by logged-on, administrative
   users).


## MAINTAINERS

Current maintainers:

* Daniel F. Kudwien (sun) - https://www.drupal.org/user/54136
* Peter Wolanin (pwolanin) - https://www.drupal.org/user/49851
* Stefan M. Kudwien (smk-ka) - https://www.drupal.org/user/48898
* Dave Reid (Dave Reid) - https://www.drupal.org/user/53892

This project has been sponsored by:

* UNLEASHED MIND
  Specialized in consulting and planning of Drupal powered sites, UNLEASHED MIND
  offers installation, development, theming, customization, and hosting to get
  you started. Visit https://www.unleashedmind.com for more information.
