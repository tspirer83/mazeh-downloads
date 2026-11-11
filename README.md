# Mazeh downloads

Files that Mazeh downloads, or that people download to install it. Mazeh translates Hebrew on screen into English: https://spirertech.com/mazeh/

This repository holds release files only. The apps' source code is not here.

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

Made by Spirer Technology Solutions LLC. Questions: support@spirertech.com
