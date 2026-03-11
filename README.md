# Naruto Shippuden Ultimate Ninja Impact HD Texture Pack

Naruto Shippuden: Ultimate Ninja Impact HD Texture Pack (PPSSPP)

This is a complete HD texture pack for Naruto Shippuden: Ultimate Ninja Impact (PSP), developed for the PPSSPP emulator.

The project was developed over more than a year, although it wasn't continuous work throughout that period (months without working on the project).

Most of the game's textures were upscaled 4x using the HDCube4Plus AI model, with several manual adjustments in cases where automatic upscaling did not produce satisfactory results.

# Project Features

AI-Powered Upscaling

All main textures were processed using the HDCube4Plus model.

After upscaling, several images required additional adjustments to correct imperfections, inconsistencies, or elements that the AI ​​model could not reconstruct correctly.

# Reconstruction of the Anime Cards

One of the most complex processes in this project was the reconstruction of the game cards, which are images based on frames from the anime.

These images in the original game have very low resolution, and AI upscaling did not produce satisfactory results.

To solve this, a much more advanced process was necessary:

1: All frames from over 200 episodes of the Naruto Shippuden anime were extracted using FFmpeg.

2: This generated millions of images.

3: A system was created in Google Colab using:

    DINOv2

    CLIP

These models were used to generate image embeddings.

After that, code was developed to semantically compare the game card images with millions of frames from the anime, allowing it to automatically find the corresponding high-quality frame.

When a matching frame was found, it directly replaced the original game texture.

This means that these images were not upscaled, as the original anime frames already have sufficient quality.

The same was not done for the images in story mode, which are also anime frames and are quite large; replacing them with anime frames wouldn't make a difference, so they received normal upscaling.

# Manual Reconstruction of Some Textures

Some specific textures in the game did not work well with AI upscaling.

In these cases, other approaches were used:

    Manually searching for high-quality promotional images on Japanese websites from the time of the game's release.

    Using internal textures from the game itself at higher resolutions to reconstruct specific parts, such as character faces.

    When neither of these options was available, generative AI was used to reconstruct certain images.

# Character Face Reconstruction

Many facial images in the game have better versions within other textures in the game itself (for example, full-body images).

Whenever possible, these versions were used to reconstruct the faces in better quality.

In cases where this was not possible, generative AI was used through the Nano Banana V2 model from Gemini.

Due to the consistency limitations of this model between different images, the consistency wasn't as good as expected, so the pack includes two versions of these textures.

# Two Versions of the Pack (AI / Without AI)

Inside the textures.ini folder there are two ini files:

    textures(AI, copy and paste into the main folder and delete this part).ini

    textures(no IA, copy and paste into the main folder and delete this part).ini

To switch between them, simply replace the corresponding .ini file.

This allows each user to choose the version they prefer to use.

# Pack Versions

The pack is available in four different versions.

PNG (Best Quality)

PNG preserves the highest quality textures, but has a greater impact on performance.

    PNG Normal

    PNG Vibrant Colors

Each one is over 2GB, so they were split into two parts for download.

# KTX2 (Better Performance)

KTX2 is a compressed format optimized for emulation.

    KTX2 Normal

    KTX2 Vibrant Colors

These versions include:

    Better performance

    Faster loading

    Smaller files (less than 2GB)
    
The visual difference compared to PNG is minimal in most cases.

# Difference from the "Vibrant Colors" Version

The Color version uses color processing that slightly increases the vibrancy and chromatic fidelity of the images.

This process was done by converting color profiles using AdobeRGB → sRGB, preserving transparency and applying maximum PNG compression.

The goal is to produce slightly more vibrant colors without distorting the original artwork.

# Known Issue in KTX2 Versions

Due to the way ktx2 was created in my package and how PPSSPP loads compressed textures, a small visual glitch of a few milliseconds may occur during rapid texture changes.

This can mainly happen:

    In character selection

    In menus that rapidly switch between images

This problem does not occur in the PNG version.

To reduce this effect, it is recommended to change the following setting in PPSSPP:

    Settings →
    Tools →
    Developer Tools →
    Texture Replacement →
    Texture Replacement Loading Speed ​​→
    Instant

This slightly reduces the visual effect of the glitch, but does not eliminate it completely.

# Installation

Extract the downloaded package

Copy the folder:

    ULES01537

to the directory:

    /PPSSPP/TEXTURES/

Open PPSSPP

Go to:

    Settings → Tools → Developer Tools

Activate:

    Replace Textures

Done.

## 📸 Interactive Comparison (Slider)

To see the real difference in quality between the original textures and the AI ​​upscale, access the interactive comparator:

👉 Screenshots : https://meskh4h4.github.io/naruto-shippuden-ultimate-ninja-impact/
