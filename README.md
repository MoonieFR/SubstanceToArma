## SubstanceToArma

These presets were created to export and adapt textures from Substance Painter to Arma 3.

## How it works:

The export parameter using the met-rough workflow exports the specular map (SMDI) like this:
R = User1 (blank)
G = Diffuse/Base Color
B = Roughness

Note that Arma uses the blue channel information to determine where it needs to shine more or less. Arma 3 doesn't support PBR, we're talking about a non-pbr workflow using specular maps. It's important to note that a specular map and a roughness map are not interpreted in the same way, but specular values can be inverted to transform a roughness map into a specular map.

If your texture is too bright and looks strange in-game, this may be due to the fact that you didn't convert your roughness to specular before exporting. 

IT'S IMPORTANT TO INVERT ROUGHNESS MAP VALUES BEFORE EXPORTING. 


## List of presets 

- Arma 3 Super (MetRough) - Preset to export CO/NOHQ/AS/SMDI maps from a pbr metallic roughness project.
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


