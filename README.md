# Basisu prebuilt binaries.

Original and official repository [here](https://github.com/BinomialLLC/basis_universal).

*Built with CMake for x86 Windows.*

------

For full usage go to [this repo](https://github.com/BinomialLLC/basis_universal).

## Basic usage.

For basic texture conversion.

```powershell
basisu x.png
```

To adjust the quality include a **-q** tag with a range of `[0-255]`, for lowest to highest quality.

```powershell
basisu x.png -q 255
```

## The .basis texture spec.

One may wonder *why* would you opt for a different texture format while `.jpg`, `.png`  and other *regular* picture formats just work. There are meant to be decoded on the **CPU**. The `.basis` file format is meant to be decoded on the **GPU**. In a game for example a .`png` will have to be decompressed by the CPU *first* then the sent to the GPU but with .`basis` textures the texture is sent directly to the GPU **as-is**. This reduces CPU overhead and amount of memory allocated on the GPU for textures. Plus .`basis` files are way smaller than their .`png` counterparts.

