minecraft
=========

Minecraft script for OpenBSD

# The Plan

1. On initial run, prompt user for location to download [Minecraft.jar](https://s3.amazonaws.com/Minecraft.Download/launcher/Minecraft.jar)
2. Create a .rc file with jar location and startup options.
3. After initial run parse .rc file to find Minecraft.jar and startup.
4. Possibly generate the ~/minecraft/launcher_profiles.json after asking user for login name?

Just tested the optoin of writing a partial ~/minecraft/launcher_profiles.json file.. totally worked

So we can prompt the user for location of Minecraft.jar and their username and write a blurb like:

```
{
  "profiles": {
    "<username>": {
      "name": "<username>",
      "javaDir": "/usr/local/bin/minecraft"
    }
  }
}
```

And Minecraft.jar will pick it up and run with it.. then the end user doesn't have to do a dance with LWJGL
