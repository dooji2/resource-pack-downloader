# Resource Downloader
### A complex Fabric Minecraft Mod to download a mod/resource pack (or more) from a URL(or multiple URLs)!
#

![a](https://i.imgur.com/NZ1z4GV.png)
#

Download your resource packs/mods from multiple URLs(or just one). It can be multiple Dropbox folders, multiple individual resource packs on Dropbox/GDrive, and more!

Please check out the following before proceeding:

<details>
<summary>Usage</summary>

Under your “config” folder, under “rpdl”, you’ll see two files, open **pack.json**. 

Inside **pack.json**, you’ll see "urlPaths" (for your URLs), "folder" (whether your URLs lead to a folder or not), “frequency”, and "hashcheck".

For example:

**pack.json**
```
{
    "urlPaths": ["https://modrinth.com/", "https://modrinth.com/mod/resource-downloader/"],
    "redownloadrp": false,
    "enableResourcePacks": false,
    "folder": true,
    "frequency":60,
    "hashcheck": false,
    "modURLs": ["https://modrinth.com/mod/resource-downloader/"],
    "redownloadmods": false,
    "remoteconf":[" "],
    "version": 1
}
```

**Please note that only Dropbox files & folders, and Google Drive files were tested. Make sure the links you put in are public.**

**Any other URL that, when accessed, directly downloads a file/folder, can be used. URLs which contain the file's filename in the URL are preferred for now.**

Now, the **“frequency”** is how often you’d like the mod to re-download the resource packs in pack.json. The default value is “60”, meaning 60 minutes. 

***An example of how the frequency works is, let’s say you put 60 minutes. When you first launch the game, the resource packs would be downloaded nonetheless, then, after 60 minutes if you launch the game again, it will download the resource packs again.***

**"hashcheck"**, if true, will dismiss the values of "folder" & "frequency", and will assume the link leads to a Dropbox folder/any .zip file which would be a resource pack. Every time Minecraft is launched, it downloads the resource pack and checks if anything has changed by comparing their hashes.

**"modURLs"** should contain one or more URLs leading to either a .zip file containing multiple mods, or multiple links leading to mods (.jar files).

**"redownloadmods"** is false by default. It determines whether mods should be downloaded the next time the game is launched. If true, on the next launch, it will redownload all of the mods from "modURLs", and will set itself to false again afterwards.

A wiki will be made soon to document other features.
</details>

<details>
<summary>A few things to note</summary>

When Minecraft is launched, it starts downloading the resource pack(s)/mods, and so Minecraft will halt until all of the resource pack(s)/mods are downloaded and placed properly onto your resourcepacks & mods folders.

After Minecraft launches, you should see all of the resource packs in there, so just apply them and you’re done! As for the mods, please restart the game.
</details>
