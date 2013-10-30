LuaPlugin
============

LuaPlugin is a simple plugin system for lua modules. With LuaPlugin you can easily manage:
1. lua module dependencies
2. lua module versions
3. lua module name conflict
4. lua module on different platforms

a typicall lua plugin directory looks like this:

<your plugin name-version>/
--|plugin.lua 
--|share/
--|res/
--|platforms/
----|iOS/
------|res/
------|native/
------|libs/
--------|x32/
--------|x64/
----|android/
------|res/
------|native/
------|libs/
--------|x32/
--------|x64/
----|java/
------|res/
------|native/
------|libs/
--------|x32/
--------|x64/

plugin.lua is a plugin description file

share/ folder contains all the lua codes, which should be shared on all the platforms

res/ folder under the plugin root, contains all the resources used in this plugin. 
They could be localization files, images, icons, etc.

platforms/ folder contains all the platform dependent code, res, and libraries. 
each platform is categoried into a subfolder. 

native/ folder is used to organise the platform specific code. For example, your objective c code for iOS, 
java code for android.

libs/ folder contains the libraries that is used in your plugin. They could be .dll, .so, .jar etc. These binary
files need to be put into x32 subfolder or x64 subfolder according to their architecture.



