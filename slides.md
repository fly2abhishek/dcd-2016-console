## Why write code, when you can use Drupal Console?  <!-- .element: class="front-title" -->
![](img/drupal-console.png) <!-- .element: class="logo" -->

Abhishek Anand



## What is console?

>The Drupal CLI. A tool to generate boilerplate code, interact with and debug Drupal.

Note: This will only appear in the speaker notes window.


## The maintainers
<table>
	<tr>
		<td>
			<img alt='jmolivas' class='img-circle' src='https://avatars.githubusercontent.com/u/366275?v=3&amp;s=140' width='140'>
			<div class='overbox'>
				<p>
					<a href='https://github.com/jmolivas' target='_blank'><i class='fa fa-github'></i></a> <a href='https://twitter.com/jmolivas' target='_blank'><i class='fa fa-twitter'></i></a> <a href='http://jmolivas.com' target='_blank'><i class='fa fa-globe'></i></a>
				</p>
			</div>
		</td>
		<td>
			<img alt='enzolutions' class='img-circle' src='https://avatars.githubusercontent.com/u/907914?v=3&amp;s=140' width='140'>
			<div class='overbox'>
				<p>
					<a href='https://github.com/enzolutions' target='_blank'><i class='fa fa-github'></i></a> <a href='https://twitter.com/enzolutions' target='_blank'><i class='fa fa-twitter'></i></a> <a href='http://enzolutions.com/' target='_blank'><i class='fa fa-globe'></i></a>
				</p>
			</div>
		</td>
		<td>
			<img alt='omero' class='img-circle' src='https://avatars.githubusercontent.com/u/1909779?v=3&amp;s=140' width='140'>
			<div class='overbox'>
				<p>
					<a href='https://github.com/omero' target='_blank'><i class='fa fa-github'></i></a> <a href='https://twitter.com/omers' target='_blank'><i class='fa fa-twitter'></i></a> 
				</p>
			</div>
		</td>
		<td>
			<img alt='dmouse' class='img-circle' src='https://avatars.githubusercontent.com/u/198571?v=3&amp;s=140' width='140'>
			<div class='overbox'>
				<p>
					<a href='https://github.com/dmouse' target='_blank'><i class='fa fa-github'></i></a> <a href='https://twitter.com/dmouse' target='_blank'><i class='fa fa-twitter'></i></a> <a href='http://dmouse.net' target='_blank'><i class='fa fa-globe'></i></a>
				</p>
			</div>
		</td>
	</tr>
	<tr>
		<td>
			<h4>
				Jesús Manuel Olivas
			</h4>
		</td>
		<td>
			<h4>
				Eduardo Garcia
			</h4>
		</td>
		<td>
			<h4>
				Omar Aguirre
			</h4>
		</td>
		<td>
			<h4>
				David Flores
			</h4>
		</td>
	</tr>
</table>
[And many more...](https://drupalconsole.com/contributors)


## How is it different from drush?
* Drupal console is a 'from the-ground-up' Drupal CLI tool that leverages Symphony CLI components and modern PHP OOP design practices. 
* Drush is a venerable Drupal CLI tool that has been around since Drupal 4.7, thus built with an older design practice.
* There is overlap based on both projects being a general purpose Drupal administration CLI tool. 
* Drush has more features, due to its age, but Drupal Console has some new features due to its more modern design.


<table>
     <thead>
          <tr>
               <th scope="col">
               <h4>Drush Features</h4>
               </th>
               <th scope="col">
               <h4>Drupal Console Features</h4>
               </th>
          </tr>
     </thead>
     <tbody>
          <tr>
               <td>
               <ul>
                    <li>Download Drupal</li>
                    <li>Download contrib modules</li>
                    <li>Install Drupal</li>
                    <li>Update Drupal and contrib module versions</li>
                    <li>Run updatedb</li>
                    <li>Clear the cache</li>
                    <li>Run cron</li>
                    <li>Run Drupal with a lightweight web server</li>
                    <li>Import, export and merge configuration</li>
                    <li>Add users and set their roles</li>
                    <li>Add permissions to roles</li>
                    <li>Back up and restore Drupal</li>
                    <li>Copy your database and files to a remote server</li>
                    <li>Compile twig templates</li>
               </ul>
               </td>
               <td>
               <ul>
                    <li>Generate code for a:
                    <ul>
                         <li>Console command</li>
                         <li>Content type</li>
                         <li>Controller</li>
                         <li>Entity</li>
                         <li>Form alter hook</li>
                         <li>Module</li>
                         <li>Field type, widget and formatter</li>
                         <li>Image effect</li>
                         <li>Rest resource</li>
                         <li>Service</li>
                         <li>Theme</li>
                    </ul>
                    </li>
                    <li>Switch maintenance mode on or off</li>
                    <li>Run unit tests</li>
               </ul>
               </td>
          </tr>
     </tbody>
</table>



## What the big deal?

* Say bye to writing your module/theme from the scratch. <!-- .element: class="fragment" -->
* Its multilingual, yes you can write cli commands in: <!-- .element: class="fragment" -->
  * हिन्दी <!-- .element: class="fragment" -->
  * मराठी  <!-- .element: class="fragment" -->
  * or 19 languages <!-- .element: class="fragment" -->
* Debug Drupal <!-- .element: class="fragment" -->



## Installing Drupal Console

Using curl:<!-- .element: class="fragment" -->

```
$ curl https://drupalconsole.com/installer -L -o drupal.phar
```
<!-- .element: class="fragment" -->
Or if you don't have curl:<!-- .element: class="fragment" -->

```
$ php -r "readfile('https://drupalconsole.com/installer');" > drupal.phar
```
<!-- .element: class="fragment" -->

#### Execute <!-- .element: class="fragment" -->

* You can now execute using: <!-- .element: class="fragment" -->
```
$ php drupal.phar
```
<!-- .element: class="fragment" -->


## Using Composer
* Install Drupal Console globally using composer:
<!-- .element: class="fragment" -->
```
$ composer global require drupal/console:@stable
```
<!-- .element: class="fragment" -->
* Add the binary directory to your class path: <!-- .element: class="fragment" -->

```
$ echo "PATH=$PATH:~/.composer/vendor/bin" >> ~/.bash_profile
```
<!-- .element: class="fragment" -->
#### Execute <!-- .element: class="fragment" -->
* You can now execute using: <!-- .element: class="fragment" -->

```
$ drupal init
```
<!-- .element: class="fragment" -->


## Install per site
It is recommended to install Drupal Console per site.  <!-- .element: class="fragment" -->
```
$ composer require drupal/console:@stable --prefer-dist --optimize-autoloaded

$ drupal init
```
 <!-- .element: class="fragment" -->


## Install in other languages
```
$ composer require drupal/console-hi:~1.0 --prefer-dist --optimize-autoloader
```
 <!-- .element: class="fragment" -->
Will install Drupal Console in Hindi.
 <!-- .element: class="fragment" -->


## Using Drupal Console

```{sh}
➜  $ drupal list
Drupal Console version 0.11.3

Usage:
  command [options] [arguments]

Options:
  -h, --help
  -q, --quiet
  -V, --version
      --ansi
      --no-ansi
  -n, --no-interaction
  -e, --env[=ENV]        The Environment name [default: "prod"]
      --root[=ROOT]      Define the Drupal root to be used in command execution
      --no-debug         Switches off debug mode
      --learning         Generate a verbose code output
  -c, --generate-chain   Shows command options and arguments as yaml output to be used in chain command
  -i, --generate-inline  Shows command options and arguments as inline command
  -d, --generate-doc     Shows command options and arguments as markdown
  -t, --target[=TARGET]  Site name you want to interact with (for local or remote sites)
  -l, --uri=URI          URI of the Drupal site to use (for multi-site environments or when running on an alternate port)
  -y, --yes              Skip confirmation and proceed
  -v|vv|vvv, --verbose

Available commands:
  _completion                       BASH completion hook.
  check                             System requirement checker
  cr                                Rebuild and clear all site caches.
  gap                               Generate an Authentication Provider
  gcm                               Generate commands for the console.
  gcn                               Generate & Register a controller
  gdd                               Generate the DrupalConsole.docset package for Dash
  gdg                               Generate documentations for Commands
  geb                               Generate a new content type (node / entity bundle)
  gecg                              Generate a new config entity
  gect                              Generate a new content entity
  ges                               Generate an event subscriber
  gfa                               Generate an implementation of hook_form_alter() or hook_form_FORM_ID_alter
  gm                                Generate a module.
  gp                                Generate module permissions
  gpb                               Generate a plugin block
  gs                                Generate service
  gt                                Generate a theme.
  help                              Displays help for a command
  init                              Copy configuration files to user home directory.
  list                              Lists commands
  self-update                       Update project to the latest version.
 cache
  cache:rebuild                     Rebuild and clear all site caches.
 generate
  generate:authentication:provider  Generate an Authentication Provider
  generate:command                  Generate commands for the console.
  generate:controller               Generate & Register a controller
  generate:doc:dash                 Generate the DrupalConsole.docset package for Dash
  generate:doc:gitbook              Generate documentations for Commands
  generate:entity:bundle            Generate a new content type (node / entity bundle)
  generate:entity:config            Generate a new config entity
  generate:entity:content           Generate a new content entity
  generate:event:subscriber         Generate an event subscriber
  generate:form                     Generate a new "FormBase"
  generate:form:alter               Generate an implementation of hook_form_alter() or hook_form_FORM_ID_alter
  generate:form:config              Generate a new "ConfigFormBase"
  generate:metatag:group            Generate a meta tag group.
  generate:metatag:tag              Generate a meta tag.
  generate:module                   Generate a module.
  generate:permissions              Generate module permissions
  generate:plugin:block             Generate a plugin block
  generate:plugin:ckeditorbutton    Generate CKEditor button plugin.
  generate:plugin:condition         Generate a plugin condition.
  generate:plugin:field             Generate field type, widget and formatter plugins.
  generate:plugin:fieldformatter    Generate field formatter plugin.
  generate:plugin:fieldtype         Generate field type plugin.
  generate:plugin:fieldwidget       Generate field widget plugin.
  generate:plugin:imageeffect       Generate image effect plugin.
  generate:plugin:imageformatter    Generate image formatter plugin.
  generate:plugin:mail              Generate a plugin mail
  generate:plugin:rest:resource     Generate plugin rest resource
  generate:plugin:rulesaction       Generate a plugin rule action
  generate:plugin:type:annotation   Generate a plugin type with annotation discovery
  generate:plugin:type:yaml         Generate a plugin type with Yaml discovery
  generate:plugin:views:field       Generate a custom plugin view field.
  generate:profile                  Generate a profile.
  generate:routesubscriber          Generate a RouteSubscriber
  generate:service                  Generate service
  generate:theme                    Generate a theme.
 locale
  locale:language:add               Add a language to be supported by your site
  locale:language:delete            Delete a language to be supported by your site
  locale:translation:status         List available translation updates
 scheduled_updates
  scheduled_updates:run_updates     Run Scheduled Update
 settings
  settings:check                    System requirement checker
  settings:init                     Copy configuration files to user home directory.
 translation
  translation:cleanup               Clean up translation files
  translation:pending               Determine pending translation string in a language or a specific file in a language
  translation:stats                 Generate translate stats
  translation:sync                  Sync translation files
 ```
 <!-- .element: class="fragment" -->


 # Thank You! 
 ## Questions? <!-- .element: class="fragment" -->
