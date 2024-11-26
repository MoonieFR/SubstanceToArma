# 🎨 Arma 3/DayZ Substance Painter Export Presets

Welcome to this collection of **Substance Painter presets** crafted to adapt your textures for **Arma 3** and **DayZ**! 

---

## ✨ Preset Overview

### Arma 3 Super

This preset uses the **metallic-roughness workflow**, configuring the SMDI (**specular map**) with the following channel setup:

- 🟥 **Red**: `User1` (White)
- 🟩 **Green**: Metallic
- 🟦 **Blue**: Roughness

It will export the following maps:
  - `$TextureSet_CO` (Color map)
  - `$TextureSet_CA` (Color Map with Alpha)
  - `$TextureSet_SMDI` (Specular map)
  - `$TextureSet_NOHQ` (Normal map)

> **Note:** This preset is straightforward and works seamlessly for both Arma 3 and DayZ.  
> **Tip:** Ignore the warning "`User1` channel is missing in your texture set"` for this preset.

---

### Other Presets


In the "OTHERS" folder, you will find other export-presets including one preset for people working with SpecGloss instead of MetRough. 

---

#### Arma 3 Super (SpecGloss)

This preset supports the **specular-glossiness workflow**, optimized for **non-PBR projects** in Arma 3. Ideal for older workflows or specific texturing requirements.

---

#### Arma 3 SuperNo2Diff (MetRough)

This preset exports CO/NOHQ/AS/SMDI maps along with **Grey OpenGL normal maps** from a **metallic-roughness project**.  
It also embeds normal details directly into the diffuse/albedo map, adding depth even without indirect lighting.

---

## Workflow Tips

### Invert Roughness for Accurate Exports

If your texture appears too bright in-game, it may be necessary to **invert the roughness** before exporting from Substance Painter. 

To make this process easier, use the included **Smart Material**:  

#### `Arma 3 - MetRough.spsm`

This Smart Material, located in the **SmartMaterial** folder, can automate roughness inversion for you.

##### Steps to Use:

1. Drag and drop the **`Arma 3 - MetRough` Smart Material** into your **Layers Window**.
2. Move all your layers into the **`Arma 3 - MetRough` folder** created by the Smart Material.

This setup ensures that roughness inversion is handled correctly for Arma 3 and DayZ.

---

### Add Depth with the AO Layer

The included Smart Material also contains an **`AO` layer**, designed to add **fake shadows** based on your Ambient Occlusion (AO) map. Properly adjusted, it enhances the depth and realism of your textures.


##### How to Use the AO Layer:

1. Ensure the **`AO` layer** is positioned **above all other layers** in your stack.
2. Adjust opacity and blending modes for the AO layer to achieve your desired effect.

> **Tip:** Experiment with settings to see how the AO layer can breathe life into your textures!

---

### Specular Power Recommendations

For optimal results, set the `specularPower` value below 60 but ti's really up to you to try and find the correct one.
This ensures better control over shine and reflection. Adjust both **specular** and **specularPower** as needed for a balanced result.

---

## How to Import Presets

### Option 1: Import via Substance Painter

1. Clone this repository and copy all files to your system.
2. Open **Substance Painter**.
3. Go to **File > Import Resources**, then select `.spexp` file.
4. Choose **Shelf** as the destination and click **Import**.

You can also drag & drop it directly into the software. 

---

### Option 2: Add Files Manually

1. Locate your Substance Painter **shelf** directory:
   - **Windows**: `C:\Users\[username]\Documents\Adobe\Adobe Substance 3D Painter\assets\export-presets`
2. Copy all `.spexp` files into the appropriate folder.

---

## Contributing

Have ideas or improvements? Feel free to contact me on Discord: **mooniefr**.  
Your contributions to these export presets are always welcome!

---

Enjoy using these custom export presets to elevate your Substance Painter projects for Arma 3 and DayZ! 🚀
