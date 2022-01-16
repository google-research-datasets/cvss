# CVSS: A Massively Multilingual Speech-to-Speech Translation Corpus

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-green.svg)](https://creativecommons.org/licenses/by/4.0/)

*CVSS* is a massively multilingual-to-English speech-to-speech translation corpus, covering sentence-level parallel speech-to-speech translation pairs from 21 languages into English. CVSS is derived from the [Common Voice](https://commonvoice.mozilla.org/) speech corpus and the [CoVoST 2](https://github.com/facebookresearch/covost) speech-to-text translation corpus. The translation speech in CVSS is synthesized with two state-of-the-art TTS models trained on the [LibriTTS](http://www.openslr.org/60/) corpus.

CVSS includes two versions of spoken translation for all the 21 x-en language pairs from CoVoST 2, with each version providing unique values:

 - *CVSS-C*: All the translation speeches are in a single canonical speaker's voice. Despite being synthetic, these speeches are of very high naturalness and cleanness, as well as having a consistent speaking style. These properties ease the modeling of the target speech and enable models to produce high quality translation speech suitable for user-facing applications.

 - *CVSS-T*: The translation speeches are in voices transferred from the corresponding source speeches. Each translation pair has similar voices on the two sides despite being in different languages, making this dataset suitable for building models that preserve speakers' voices when translating speech into different languages.

Together with the source speeches originated from Common Voice, they make two multilingual speech-to-speech translation datasets each with about 1,900 hours of speech.

In addition to translation speech, CVSS also provides normalized translation text matching the pronunciation in the translation speech (e.g. on numbers, currencies, acronyms, etc.), which can be used for both model training as well as standardizing evaluation.

Please check out [our paper](https://arxiv.org/abs/2201.03713) for the detailed description of this corpus, as well as the baseline models we trained on both datasets.


## Getting the data

The translation speech and the normalized translation text in CVSS can be downloaded from the links in the following table:

| Source language | Code | CVSS-C | CVSS-T |
| --------------- |:----:|:------:|:------:|
| Arabic          |  ar  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_ar_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_ar_en_v1.0.tar.gz) |
| Catalan         |  ca  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_ca_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_ca_en_v1.0.tar.gz) |
| Welsh           |  cy  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_cy_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_cy_en_v1.0.tar.gz) |
| German          |  de  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_de_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_de_en_v1.0.tar.gz) |
| Estonian        |  et  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_et_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_et_en_v1.0.tar.gz) |
| Spanish         |  es  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_es_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_es_en_v1.0.tar.gz) |
| Persian         |  fa  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_fa_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_fa_en_v1.0.tar.gz) |
| French          |  fr  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_fr_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_fr_en_v1.0.tar.gz) |
| Indonesian      |  id  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_id_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_id_en_v1.0.tar.gz) |
| Italian         |  it  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_it_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_it_en_v1.0.tar.gz) |
| Japanese        |  ja  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_ja_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_ja_en_v1.0.tar.gz) |
| Latvian         |  lv  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_lv_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_lv_en_v1.0.tar.gz) |
| Mongolian       |  mn  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_mn_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_mn_en_v1.0.tar.gz) |
| Dutch           |  nl  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_nl_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_nl_en_v1.0.tar.gz) |
| Portuguese      |  pt  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_pt_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_pt_en_v1.0.tar.gz) |
| Russian         |  ru  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_ru_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_ru_en_v1.0.tar.gz) |
| Slovenian       |  sl  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_sl_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_sl_en_v1.0.tar.gz) |
| Swedish         |  sv  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_sv_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_sv_en_v1.0.tar.gz) |
| Tamil           |  ta  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_ta_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_ta_en_v1.0.tar.gz) |
| Turkish         |  tr  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_tr_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_tr_en_v1.0.tar.gz) |
| Chinese         |  zh  | [link](https://storage.googleapis.com/cvss/cvss_c_v1.0/cvss_c_zh_en_v1.0.tar.gz) | [link](https://storage.googleapis.com/cvss/cvss_t_v1.0/cvss_t_zh_en_v1.0.tar.gz) |

Each `tar.gz` file in the links above includes `train`, `dev` and `test` directories containing audio clips as the translation speech, as well as `train.tsv`, `dev.tsv` and `test.tsv` files containing the normalized translation text. The normalized translation text files included in CVSS-C and CVSS-T are identical.

These translation audio clips and translation texts are to be paired with the [Common Voice](https://commonvoice.mozilla.org/en/datasets) release version 4 (required) based on the audio file names. If you need the original translation text without the normalization, they are provided by [CoVoST 2](https://github.com/facebookresearch/covost).


## License

CVSS is released under the very permissive [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.


## Citation

Please cite this paper when referencing the CVSS corpus:

```
@misc{jia2022cvss,
    title={{CVSS} Corpus and Massively Multilingual Speech-to-Speech Translation},
    author={Jia, Ye and Tadmor Ramanovich, Michelle and Wang, Quan and Zen, Heiga},
    eprint={2201.03713},
    archivePrefix={arXiv},
    year={2022}
}
```
