## Project ( app ) file structure


```
server/ #( project server sider folder )
- controllers/
- models/
- emails/ #(Email templates)
- forms/ #(JSON forms)
- helpers/
- templates/ #(HBS templates)
- widgets/
bin/
- [project script files for run in terminal]
config/ #( we.js project config folder )
- local.js ( local config file )
- [others config files]
- locales/ #( node i18n locales files used in client and server )
- - [locale].json
files/
- public/ #( public default production assets folder )
test/ #( tests folder with mocha )
- integration/
- - api/ #( serverside api tests )
- - - [mocha test files]
- bootstrap.js
- mocha.opts
bower.json (optional)
package.json
app.js
plugin.js (optional)
node_modules/ #(node modules folder)
- [npm modules, plugins and theme folders]

```

## Plugin file structure

Plugins is found inside node_modules folder

```
lib/ ( npm module folder )
- index.js ( initial file how load in with require )
locales/ ( json default locales )
server/ ( we.js server files )
- controllers/
- models/
- emails/ #(email templates)
- forms/ #(json forms)
- helpers/
- templates/ #(hbs templates)
- widgets/
files/
- public/ #( public default production assets folder )
README.md
package.json
plugin.js ( you plugin file )
```

## Theme file structure

Themes is found inside node_modules folder

```
files/ ( files folder )
files/public/ ( public folder )
files/public/scripts.js ( default theme script folder )
files/public/style.css ( default theme css file )
templates/ ( server side templates )
templates/email/ ( nodemailer templates )
templates/server/ (server side templates)
templates/server/html.hbs (html structure file)
templates/server/partials/ (default partials folder)
templates/server/layouts/ (default layouts folder)
README.md
package.json
theme.js ( you theme config file )
```
