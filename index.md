# Introduction
Skia is google developed amazing 2d graphics library. The official doc is [https://skia.org/docs/](https://skia.org/docs/), but i feel it is not comprehensive, so i got motivated to have one.

# OS Guidance
As of now this doc is based on windows only.

# Download Skia
You can download skia by following intstructions from [https://skia.org/docs/user/download/](https://skia.org/docs/user/download/).

# Build Skia
Skia can be build by following instructions from [https://skia.org/docs/user/build/](https://skia.org/docs/user/build/).

# Use Skia
Downloading and building skia is very time taking, and complex task. I already have build skia based on milestone 149. You can download it from [my google drive](https://drive.google.com/file/d/1ZNvqQbNT0D6eydupOBWNH7xpy0c1d8Bc/view?usp=sharing).

# Setup
To use skia you need:
1. Visual Studio 2026(current version as of April, 2026)
2. Skia build. Build your own or download from above link.

# Setup Visual Studio
1. Create a win32 c++ desktop project.
2. I am assuming you have downloaded or build the skia and put at F:\skiaCombined
3. Set
```
F:\skiaCombined\skia;F:\skiaCombined\skia\third_party\externals\dawn\include;F:\skiaCombined\skia\out\combined\gen;F:\skiaCombined\skia\out\combined\gen\third_party\dawn\include;
```
as additional include directories.
4. Set
```
F:\skiaCombined\skia\out\combined;F:\skiaCombined\skia\out\combined\cmake_dawn\src\dawn
```
as additional lib directories.

The Skia Build should be look like below
- `F:\skiaCombined`
  - `skia`
    - `include`
      - `android`
      - `codec`
      - `config`
      - `core`
      - `docs`
      - `effects`
      - `encode`
      - `gpu`
      - `pathops`
      - `ports`
      - `private`
      - `sksl`
      - `svg`
      - `third_party`
      - `utils`
    - `modules`
      - `audioplayer`
      - `bentleyottmann`
      - `canvaskit`
      - `jsonreader`
      - `pathops`
      - `skcms`
      - `skottie`
      - `skparagraph`
      - `skplaintexteditor`
      - `skresources`
      - `sksg`
      - `skshaper`
      - `skunicode`
      - `svg`
    - `out`
      - `combined`
        - `bentleyottmann.lib`
        - `compression_utils_portable.lib`
        - `dawn_combined.lib`
        - `expat.lib`
        - `harfbuzz.lib`
        - `icu.lib`
        - `jsonreader.lib`
        - `libjpeg.lib`
        - `libjpeg12.lib`
        - `libjpeg16.lib`
        - `libpng.lib`
        - `libwebp.lib`
        - `libwebp_sse41.lib`
        - `skcms.lib`
        - `skia.lib`
        - `skottie.lib`
        - `skparagraph.lib`
        - `skresources.lib`
        - `sksg.lib`
        - `skshaper.lib`
        - `skunicode_core.lib`
        - `skunicode_icu.lib`
        - `svg.lib`
        - `tint_combined.lib`
        - `wuffs.lib`
        - `zlib.lib`
        - `cmake_dawn`
          - `src`
            - `dawn`
              - `dawn_proc.lib`
    - `src`
      - `android`
      - `base`
      - `capture`
      - `codec`
      - `core`
      - `effects`
      - `encode`
      - `gpu`
      - `image`
      - `lazy`
      - `opts`
      - `pathops`
      - `pdf`
      - `ports`
      - `sfnt`
      - `shaders`
      - `sksl`
      - `svg`
      - `text`
      - `utils`
      - `xml`
      - `xps`
    - `third_party`
      - `externals`
