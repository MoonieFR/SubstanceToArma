## SubstanceToArma

These presets were created to export and adapt textures from Substance Painter to Arma 3.

## How it works:


Arma 3 Super BC (MetRough)

The export setting using the met-rough workflow exports the specular map (SMDI) as follows:
R = User1 (white)
G = Diffuse/base color
B = Roughness

Adapted to a workflow that revolves around Base Color. Not recommended for beginners. 



Arma 3 Super M (MetRough)

The export setting using the met-rough workflow exports the specular map (SMDI) as follows:
R = User1 (white)
G = Metallic
B = Roughness

Fast, easy but you will lose details.



Note that the engine uses the blue channel of this map to determine where it should shine more or less, that's why we're including the roughness in the blue channel. Arma 3 doesn't support PBR, so we're talking about a non-PBR workflow using  only specular maps. **Glossiness maps and roughness maps are not interpreted in the same way**, but values can be inverted to transform a roughness map into a glossiness.

If your texture is too bright and looks strange in the game, it may be because you didn't invert your roughness before exporting it. 
It may also be due to high values in your RVMAT. I usually recommend to keep the `specularPower` below `60`. 
The specular and specular power values are the fields you need to adjust. 

## How to invert your roughness in substance :

- Select all your layers, right-click on one of them and select `Group layers`. It will create a new folder with all your layers inside of it. 
- Right-click on the folder and select `Add levels`
- Change the `Affected Channel` from `Base Color` to `Roughness`

You can uncheck this option if you wish to continue working on your project, and re-activate it before exporting.


## List of presets 

- Arma 3 Super M (MetRough) - Preset to export CO/NOHQ/AS/SMDI maps from a pbr metallic roughness project (M for Metallic)
- Arma 3 Super BC (MetRough) - Preset to export CO/NOHQ/AS/SMDI maps from a pbr metallic roughness project (BC for Base Color).
- Arma 3 Super (SpecGloss) - Preset to export CO/NOHQ/AS/SMDI maps from a non-pbr specular glossiness project.
- Arma 3 SuperAlpha (MetRough) - Preset to export CA/NOHQ/AS/SMDI maps including alpha information from a pbr metallic roughness project.
- Arma 3 SuperAlpha (SpecGloss) - Preset to export CA/NOHQ/AS/SMDI maps including Alpha information from a non-pbr specular glossiness project.
- Arma 3 SuperNo2Diff (MetRough) - Preset to export CO/NOHQ/AS/SMDI (+ Grey OpenGL normal) maps from a pbr metallic roughness project.

Don't pay attention to the following warning: "'User1' channel is missing in your texture set."

## About SuperNo2Diff 
I use this preset when I want to include my normal info into the diffuse/albedo/colormap. Including this information is convenient because it allows you to give an illusion of depth even without indirect light.
You can also do that directly in Substance Painter but it's more tricky.

## How to import:
- Clone this repository and copy all files.
- Open Substance Painter
- Go to "File" > "Import ressources" then select all *spexp* files.
- Choose to import the ressources into your "shelf" then press "Import".

You can also:
- Go to the Substance Painter shelf located in your Documents.
     Windows: C:\Users\*username*\Documents\Substance Painter\shelf\export-presets.
     Mac OS: Macintosh > Users > *username* > Documents > Substance Painter > shelf > export-presets.
- Paste all *spexp* files.


<img src="https://cdn.discordapp.com/attachments/547997340288548874/763912413862821898/exemple.jpg">


