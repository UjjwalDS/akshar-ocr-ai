# Third-party notices

Akshar OCR AI includes these open-source components:

- **Tesseract.js 7.0.0** — Apache License 2.0
- **Tesseract.js Core 7.0.0** — Apache License 2.0
- **PDF.js 5.6.205** — Apache License 2.0
- **Tesseract OCR 5.5.2** — Apache License 2.0
- **Sanscript.js 1.3.3** — MIT License
- **English frequency data derived from wordfreq 3.1.1**, Robyn Speer — CC BY-SA 4.0 (data); Apache 2.0 (upstream code)

The bundled files remain subject to their respective licenses. Language trained-data files are downloaded on demand from the Tesseract.js data packages and are subject to the licensing information distributed with those packages.

Optional output translation uses Google's public translation endpoint and requires an internet connection. It is separate from the local Tesseract OCR engine.

Sanscript.js provides offline phonetic transliteration between Roman input and Indian scripts. Its project is https://github.com/indic-transliteration/sanscript.js and the complete MIT license is bundled at `vendor/SANSCRIPT-LICENSE.txt`.

The comparison EXE does not bundle or run NE-OCR.

english-words.json is a filtered, rounded table derived from wordfreq English data and is distributed under CC BY-SA 4.0: https://creativecommons.org/licenses/by-sa/4.0/. Original project: https://github.com/rspeer/wordfreq. Attribution: Robyn Speer (2022), https://doi.org/10.5281/zenodo.7199437. The source data credits Google Books Ngrams, Leeds Internet Corpus, Wikipedia, ParaCrawl, OPUS/OpenSubtitles, and SUBTLEX (Marc Brysbaert et al., freely available data). Full upstream source acknowledgements, citations and notices are included in vendor/WORDFREQ-SOURCES.txt; the upstream code license is vendor/WORDFREQ-LICENSE.txt.
