# First Steps


## Compiling the Cinema 4D SDK Example Project

All fresh Cinema 4D installations come pre-bundled with a bunch of SDK example
projects. They look something like this once they're compiled:  
![](http://i.imgur.com/SpXEh2a.png)

However, they aren't visible in the C4D interface by default. This is because
most of them are just sketches of finished tools and commands and they're
quite rough around the edges. C4D's developers don't want any old user to
run into these.

That said, they will be the starting point for almost all of our development
efforts. So let's go through the process of compiling them now.

### Backup the SDK Example Project
It's always a good idea to backup a clean copy of your SDK example projects
folder before starting development. Otherwise you'll have to re-install C4D
to get a clean copy: _not ideal_.

1. Open Finder
1. Navigate to `/Applications/Maxon/Cinema 4D R16/plugins/`  
![](http://i.imgur.com/oxmFVeR.png)
1. Create a new directory named `BACKUP`  
![](http://i.imgur.com/goyOPfX.png)
1. Select the `cinema4dsdk` directory and copy it (`Cmd + C`).  
![](http://i.imgur.com/pe0zxhn.png)
1. Go into the `BACKUP` directory and paste your copy there  
![](http://i.imgur.com/TaX3sRb.png)


### Open the SDK Examples Xcode Project

1. Navigate to your `plugins/cinema4dsdk` directory (**not** the one in `BACKUP`).  
![](http://i.imgur.com/O4yL97E.png)
1. Open the `cinema4dsdk.xcodeproj` project file.  
![](http://i.imgur.com/hqTlFOm.png)


### Build / Compile the Project

1. If it's open, close Cinema 4D. `TODO: See if this is just superstition`
1. Press the Play/Build button in the upper left (or hit `Cmd + B` or
  select `Product > Build`)
![](http://i.imgur.com/WjOGGzK.png)
1. You should see a "Build Succeeded" message.
1. If you see any errors, do your best to Google and debug. If you find yourself
stuck, try to Google and debug. If that doesn't work, head over to the [PluginCafe
Forums](http://www.plugincafe.com/forum/default.asp) and [ask for help](http://www.plugincafe.com/forum/new_topic_form.asp?FID=4) there.
