# Resource Pack Downloader
### A Minecraft (fabric-only) mod to download a resource pack (or more) from a URL!
#

![a](https://i.imgur.com/NZ1z4GV.png)
#

Download your resource packs from multiple URLs(or just one). It can be multiple Dropbox folders, multiple individual resource packs on Dropbox/GDrive, and more!

Please check out the following before proceeding:

<details>
<summary>Usage</summary>

Under your “config” folder, under “rpdl”, you’ll see two files, open **pack.json**. 

Inside **pack.json**, you’ll see "urlPaths" (for your URLs), "folder" (whether your URLs lead to a folder or not), “frequency”, and "hashcheck".

For example:

**pack.json**
```
{
    "urlPaths": ["https://modrinth.com/", "https://modrinth.com/mod/resource-pack-downloader/"],
    "folder": true,
    "frequency":60,
    "hashcheck": false
}
```

**Please note that only Dropbox files & folders, and Google Drive files were tested. Make sure the links you put in are public.**

**Any other URL that, when accessed, directly downloads a file/folder, can be used.**

Now, the **“frequency”** is how often you’d like the mod to re-download the resource packs in pack.json. The default value is “60”, meaning 60 minutes. 

***An example of how the frequency works is, let’s say you put 60 minutes. When you first launch the game, the resource packs would be downloaded nonetheless, then, after 60 minutes if you launch the game again, it will download the resource packs again.***

**"hashcheck"**, if true, will dismiss the values of "folder" & "frequency", and will assume the link leads to a Dropbox folder/any .zip file which would be a resource pack. Every time Minecraft is launched, it downloads the resource pack and checks if anything has changed by comparing their hashes.

As features expand, a wiki will come soon. For now, this should do.
</details>

<details>
<summary>A few things to note</summary>

When Minecraft is launched, it starts downloading the resource pack(s), and so Minecraft will halt until all of the resource pack(s) are downloaded and placed properly onto your resourcepacks folder.

After Minecraft launches, you should see all of the resource packs in there, so just apply them and you’re done!
</details>
