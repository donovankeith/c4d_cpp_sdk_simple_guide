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
  > Don't use the `plugins` directory in your preferences folder for C++ SDK development
    as the Xcode project depends on the `Framework` being located near the `plugins`
    directory.

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
1. Ensure that your destination is `My Mac (64-bit)`  
![](http://i.imgur.com/LxRsDJD.png)
1. Press the Play/Build button in the upper left (or hit `Cmd + B` or
  select `Product > Build`)
![](http://i.imgur.com/WjOGGzK.png)
1. The build will start and you'll see something like:  
![](http://i.imgur.com/gLml7pg.png)
1. Eventually, you should see a "Build Succeeded" message.
1. You should now have a `cinema4dsdk.dylib` file in your `cinema4dsdk` directory.  
![](http://i.imgur.com/zzShzSV.png)  
This is the "plugin" file that you would need to distribute to users if you
wanted them to be able to use the SDK examples without having to build them
themselves.

> **A Note About C++ vs Python and C.O.F.F.E.E. Plugins**  
C++ is a compiled language. Which means that for your plugins to run on a given
platform, they have to be specifically built for that platform. Running this
build for Mac OS 64, means it will only run on 64-bit Mac installs, not 32-bit,
and definitely not on a Windows PC. If you plan to distribute your plugin widely
you'll need to get access to every sort of computer you'll want your plugin to
run on. You'll also need to re-build every single time you update your source
code, for every single destination platform. What a pain...

> Python and C.O.F.F.E.E. are both scripting languages. Which means
that you distribute the source files, and they are interpreted on-load in C4D.
This has the benefit of making your plugins instantly cross-platform with no
need to compile.

> So why would you ever use C++ instead of Python? Well, C++ plugins typically
execute faster, and you have much greater access to different parts of C4D. So,
for anything performance critical (like tools that will interact with lots of objects),
or that needs to use a part of the SDK only available in C++ use the C++ SDK.
For everything else: save yourself a lot of grief, and just develop in Python.

### Verify in Cinema 4D

1. Open Cinema 4D.
> Make sure it's the same one whose plugin folder you used, not some other version.

1. Go to `Plugins > Cinema4dsdk` and tear off the palette.  
![](http://i.imgur.com/NaV76Ul.png)


#### Troubleshooting

If you run into build errors, or despite a "successful" build the example
plugins aren't showing up, there's a chance that your SDK project was corrupted
at some point.

In that case your best course of action, as painful as it seems, is to start
with a clean install of Cinema 4D.

If that doesn't work, do your best to Google and debug. If you're still stuck
 head over to the [PluginCafe Forums](http://www.plugincafe.com/forum/default.asp)
 and [ask for help](http://www.plugincafe.com/forum/new_topic_form.asp?FID=4) there.

### Congratulations!

Congratulations! If you've gotten this far, it mean's you've successfully built
the Cinema 4D SDK Example Projects - a feat that has taken me countless hours of
banging my head against the wall to accomplish. I hope that it was easier for you
than it was for me.


#### Your Reward

Remember how I said that the C4D Developers don't want any old user playing
with the SDK example plugins? Well, because you've passed the "developer test"
you get to play around with some pretty cool objects and tools, like:

* Drop to Surface Effector  
![](http://i.imgur.com/1pF7JJK.png)
* Liquid Painting Tool  
![](http://i.imgur.com/58lEybY.png)
