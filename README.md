# Mazeh downloads

Files that Mazeh downloads, or that people download to install it. Mazeh translates Hebrew on screen into English, and on Windows also into Russian or French: https://spirertech.com/mazeh/

This repository holds release files only. The apps' source code is not here.

## Mazeh for Windows

The newest setup program, for Windows 11 on x64 and ARM64 PCs: https://github.com/tspirer83/mazeh-downloads/releases/latest/download/Mazeh-Setup.exe

## Translation model for Windows

The release `opus-mt-tc-big-he-en-int8-v1` holds the Hebrew to English translation model that Mazeh for Windows runs on the PC. Nothing is sent anywhere to translate.

- It is **OPUS-MT `opus-mt-tc-big-he-en`**, made by the Language Technology Research Group at the University of Helsinki (Helsinki-NLP) and published at https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-he-en (revision `134c5a850dcaa763eec85bd1f4eb25112fecedbb`) under the Creative Commons Attribution 4.0 International licence: https://creativecommons.org/licenses/by/4.0/
- Changes made here: the model was converted to the ONNX format, its weights were reduced to 8-bit integers (dynamic quantisation), and its two decoder graphs were merged into one file. `source.spm`, `target.spm` and `vocab.json` are unchanged.
- The converted files are offered under the same licence, CC BY 4.0.

The model's authors ask for these to be cited:

- Jörg Tiedemann and Santhosh Thottingal, "OPUS-MT – Building open translation services for the World", EAMT 2020
- Jörg Tiedemann, "The Tatoeba Translation Challenge – Realistic Data Sets for Low Resource and Multilingual MT", WMT 2020

| File | Bytes | SHA-256 |
|---|---|---|
| `encoder.int8.onnx` | 138724329 | `d70e542a9ef186953e64151ec11c17b9e8f775feabcf7eebec7bbdd2caef2493` |
| `decoder.int8.onnx` | 226371225 | `ab88c5d40e6cc705bbb6e319bffa9761e127dfa02a6ef64fc7fcfa1d1eabd908` |
| `source.spm` | 881489 | `13dabf370542066abcfd660e72887d0ce1296a04e15913d2ec47793656434257` |
| `target.spm` | 799154 | `da28ecbe4e59653b716708410b78edbd9fd639978f01002e2a8bc9319b1ee933` |
| `vocab.json` | 2072892 | `abe93c914993f4dd8c10a7ff9cd97e813fcd1dd28dafb539504b509d8ad6183f` |

## Translation models for Russian and French

Mazeh for Windows reaches Russian and French through English: the Hebrew to English model above, then one of the two models below, also on the PC. A copy of Mazeh fetches one of them only when its owner picks that language.

Both are made by the Language Technology Research Group at the University of Helsinki (Helsinki-NLP) and published under the Creative Commons Attribution 4.0 International licence: https://creativecommons.org/licenses/by/4.0/

- The release `opus-mt-tc-big-en-zle-int8-v1` is **OPUS-MT `opus-mt-tc-big-en-zle`**, English to Russian, Ukrainian and Belarusian, published at https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-en-zle (revision `708be1d372fe4c358a352f404e6dc9ca0126ba48`). Mazeh asks it for Russian
- The release `opus-mt-tc-big-en-fr-int8-v1` is **OPUS-MT `opus-mt-tc-big-en-fr`**, English to French, published at https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-en-fr (revision `6e062862ced6f5622a589ab2aadc2a1d4978db78`)
- Changes made here, the same for both: the model was converted to the ONNX format, its weights were reduced to 8-bit integers (dynamic quantisation), and its two decoder graphs were merged into one file. `source.spm`, `target.spm` and `vocab.json` are unchanged.
- The converted files are offered under the same licence, CC BY 4.0. The authors ask for the same two papers to be cited as for the Hebrew to English model.

`opus-mt-tc-big-en-zle-int8-v1`:

| File | Bytes | SHA-256 |
|---|---|---|
| `encoder.int8.onnx` | 140063720 | `1361c4babcffa5245986d27a2e67f075132f95c2453b6c56fec1216d6c4d5271` |
| `decoder.int8.onnx` | 229055235 | `defa464607de4b9268aea32c61844ae592e55a7e1dc4cd304b9c9350f7e48ec8` |
| `source.spm` | 802747 | `3612abfe04bf08344ba91115f0e15e228a7a15a621ea856bfd548097dbaeb43c` |
| `target.spm` | 1017004 | `22940e744b3a9fd166a04880938fb61f7dfa8ba4b5d2d3f6371a6c4ba8f3b019` |
| `vocab.json` | 2510527 | `41dbdff4a0b5a6ab125715c3342c5ce6516e93ffd49608813240403f036c5efb` |

`opus-mt-tc-big-en-fr-int8-v1`:

| File | Bytes | SHA-256 |
|---|---|---|
| `encoder.int8.onnx` | 131298274 | `d50153b00883a575ff021a232363b62f20c7e4c6251c2bc4dd0a7266d609cd0c` |
| `decoder.int8.onnx` | 211490113 | `73deb06c19744acec8087cb61f1c1f0a5c3c6b113dadac6d40f1b27eda2265a8` |
| `source.spm` | 802408 | `18bb5a422a53a0bd699b005c8086cbd58a85c4be427fd57ca687c958588edcc9` |
| `target.spm` | 819955 | `6437b5600d2ae14888939e589773b09bc667c77e81326e20e3f57698a4078593` |
| `vocab.json` | 1332010 | `2994b7def69d6495d8f02369b57e3f04e2474f76ce64eda2921643e1f76fef41` |

Made by Spirer Technology Solutions LLC. Questions: support@spirertech.com
