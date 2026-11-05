# Create TextureHub.json files
without this files, you cannot add options in your pack

Create json file and name it `texturehub.json`
add this code inside of the json files
```
{
  "name": "your settings",
  "creator": "Your name",
  "version": "1.0.0",
  "options": [
    { "id": "id", "name": "your settings", "description": "description" }
  ]
}
```
you can add more options to it
```
{
  "name": "Test Pack",
  "creator": "Your name",
  "version": "1.0.0",
  "options": [
    {
      "id": "one for Example",
      "name": "example 1",
      "description": "put smth here"
    },
    {
      "id": "two for example",
      "name": "example 2",
      "description": "put another smth here",
      "default": true/false
    }
```
# Create options folders
without this folder, you cannot add options in your pack

create folder named `options`, add folder of your ID on Texturehub.json files and add the texture inside of the ID folder.
**path**

`C:\Program Files (x86)\Steam\steamapps\common\Geometry Dash\geode\config\geode.texture-loader\packs\yourpack.zip\your pack\options\folder that has ID`.
put your texture.png and texture.pnglist files

if you`re still didn't understand, please look into video tutorial

happy settings :3
