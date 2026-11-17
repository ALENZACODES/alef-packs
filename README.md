# ALEF Language Packs

![Rimon, a small round pomegranate character, standing on a pile of unmarked gift packs](docs/social-preview.png)

Static files for the ALEF Talk screen: two small Hebrew and English translation models (OPUS-MT, Apache-2.0) and the WebAssembly runtime that runs them (onnxruntime-web, MIT). Built from the ALEF repository with `node tools/talk/nmt/export-host.mjs`. Nothing here is edited by hand.

The `audio/f/israeli/` folder holds the woman's Israeli voice clips, copied from the same folder in the ALEF repository. The
app plays them from this repository's GitHub Pages address. One GitHub Pages site may hold at most 1 GB, so the other large
voice folders live in the `alef-audio` repository.

## Vowel mark packs

The `nikud/` and `phonemes/` folders hold the optional on-device packs for adding vowel marks and a sound line. Each folder has a `pack.json` list and 16 MiB parts. They are downloaded only when a learner presses Get on the ALEF site, from `https://alenzacodes.github.io/alef-packs/nikud/pack.json` and `https://alenzacodes.github.io/alef-packs/phonemes/pack.json`.

## Project structure

```text
alef-packs/
├── _nmt/                   # Hebrew and English translation models (23 files)
├── _ort/                   # WebAssembly runtime (onnxruntime-web) (4 files)
├── audio/                  # Woman's Israeli voice clips (15449 files)
├── docs/                   # Social preview image
│   └── social-preview.png
├── nikud/                  # Vowel-mark pack parts (20 files)
├── phonemes/               # Sound-line pack parts (20 files)
├── .nojekyll
├── index.html              # Pages landing file
└── README.md               # This file
```
