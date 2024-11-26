# 🎨 Arma 3/DayZ Substance Painter Export Presets

Welcome to this collection of **Substance Painter presets** crafted to adapt your textures for **Arma 3** and **DayZ**! These presets streamline the workflow by exporting maps tailored to Arma 3/DayZ.

---

## ✨ Preset Overview

### Arma 3 Super BC (MetRough)

This export uses the **metallic-roughness workflow**, configuring the SMDI (**specular map**) with the following channel setup:

- 🟥 **Red**: `User1` (White)
- 🟩 **Green**: Diffuse/Base Color
- 🟦 **Blue**: Roughness

> **For Advanced Users**: This preset emphasizes the **Base Color** channel and is not recommended for beginners.

---

### Arma 3 Super M (MetRough)

A simplified metallic-roughness workflow that also configures the **SMDI map**, offering a quicker setup for fast exports:

- 🟥 **Red**: `User1` (White)
- 🟩 **Green**: Diffuse/Base Color
- 🟦 **Blue**: Roughness

> **Note:** The blue channel controls shine intensity in Arma 3, making roughness essential. Since Arma 3 doesn’t support PBR directly, these workflows use **non-PBR specular maps**.

---

### Arma 3 Super (SpecGloss)

This preset supports the **specular-glossiness workflow**, optimized for **non-PBR projects** in Arma 3.

---

### Arma 3 SuperAlpha (MetRough)

Exports maps from a **metallic-roughness project**, with added support for **alpha information**.

---

### Arma 3 SuperAlpha (SpecGloss)

Exports maps with **alpha support** from a **specular-glossiness project**.

---

### Arma 3 SuperNo2Diff (MetRough)

This preset exports CO/NOHQ/AS/SMDI maps plus **Grey OpenGL normal maps** from a **metallic-roughness project**. It includes normal details directly in the diffuse/albedo map, creating depth in-game without indirect lighting.

> **Tip:** Ignore the warning "`User1` channel is missing in your texture set" for this preset.

---

## Workflow Tips

### Invert Roughness for Accurate Exports

If your texture appears too bright in-game, **invert the roughness** before exporting from Substance Painter. 

You can use the provided SmartMaterial named **`Arma 3 - MetRough.spsm`**, located in the **SmartMaterial** folder, to help you with this process.

#### Steps:

1. Drag and drop the **`Arma 3 - MetRough` Smart Material** into your **Layers Window**.
2. Move all your layers into the **`Arma 3 - MetRough` folder** created by the Smart Material.

This will apply the necessary adjustments automatically.

---

### Add Depth with the AO Layer

Inside the Smart Material, you will also find a layer named **`AO`**. This layer is designed to add **fake shadows** based on your Ambient Occlusion (AO) map. Properly adjusted, it brings depth and life to your textures.

#### How to Use the AO Layer:

1. Ensure the **`AO` layer** is located **above all other layers** in the Smart Material.
2. Experiment with opacity and blending modes to achieve the desired effect.

> **Tip:** Try it out for yourself—this simple addition can make a significant difference to the final look of your textures!

---

### Specular Power Recommendations

For best results, keep `specularPower` below 60. Adjust **specular** and **specularPower** values as needed for optimal shine and reflection.

---

## How to Import

### Method 1: Importing via Substance Painter

1. Clone this repository and copy all files.
2. Open **Substance Painter**.
3. Go to **File > Import Resources** and select all `.spexp` files.
4. Choose **Shelf** as the destination and click **Import**.

---

### Method 2: Manually Adding Files

1. Locate the Substance Painter shelf directory:
   - **Windows**: `C:\Users\[username]\Documents\Substance Painter\shelf\export-presets`
   - **Mac OS**: `Macintosh HD > Users > [username] > Documents > Substance Painter > shelf > export-presets`
2. Paste all `.spexp` files into this folder.


---

## Contributing

Your contributions are welcome! If you have improvements or additional workflows for Arma 3, feel free to contact me on discord: mooniefr

---

Enjoy using these custom export presets!
