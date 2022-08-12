# Indonesian TTS using Coqui TTS

Models are available in [Releases](https://github.com/Wikidepia/indonesian-tts/releases/) tab.

**DO NOT USE FOR COMMERCIAL PURPOSES!**

## Model changelog

### v1.2 (Aug 12, 2022)

Finetuned from v1.1 model on:

- 4 hours of Audiobook dataset
- 2000 sample of Azure TTS
- High quality TTS data for Javanese & Sundanese

### v1.1 (Aug 6, 2022)

Finetuned from LJSpeech model on:

- 4 hours of Audiobook dataset
- 2000 sample of Azure TTS

### v1.0 (Jun 23, 2022)

Trained from scratch on:

- 4 hours of Audiobook dataset.

## Example

`Ardi (Azure)`:

https://user-images.githubusercontent.com/72781956/183240414-b1127e83-6ddd-427c-b58d-386c377f15b4.mp4

`Gadis (Azure)`:

https://user-images.githubusercontent.com/72781956/183240420-a5d0d335-af4a-4563-a744-40f6795955c5.mp4

`Wibowo (Audiobook)`:

https://user-images.githubusercontent.com/72781956/183240434-fb0c3656-8673-453e-8900-f4df491e0d0b.mp4

## How to use

You need [`g2p-id`](https://github.com/Wikidepia/g2p-id) to convert grapheme to phoneme. 

Use `tts` command from Coqui TTS to synthesize speech:

```
tts --text "saja səˈdanʔ ˈbərada di dʒaˈkarta." \
    --model_path checkpoint.pth \
    --config_path config.json \
    --speaker_idx wibowo \
    --out_path output.wav
```

You can get all speaker idx by using `--list_speaker_idxs`:

```
tts --model_path checkpoint.pth \
    --config_path config.json \
    --list_speaker_idxs
```

## Data

- [Indonesian Azure TTS](https://depia.wiki/files/azure-tts.tar)

## Citations

```bibtex
@misc{https://doi.org/10.48550/arxiv.2106.06103,
  doi = {10.48550/ARXIV.2106.06103}, 
  url = {https://arxiv.org/abs/2106.06103},
  author = {Kim, Jaehyeon and Kong, Jungil and Son, Juhee},
  keywords = {Sound (cs.SD), Audio and Speech Processing (eess.AS), FOS: Computer and information sciences, FOS: Computer and information sciences, FOS: Electrical engineering, electronic engineering, information engineering, FOS: Electrical engineering, electronic engineering, information engineering},
  title = {Conditional Variational Autoencoder with Adversarial Learning for End-to-End Text-to-Speech},
  publisher = {arXiv},
  year = {2021},
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```

```bibtex
@inproceedings{kjartansson-etal-tts-sltu2018,
    title = {{A Step-by-Step Process for Building TTS Voices Using Open Source Data and Framework for Bangla, Javanese, Khmer, Nepali, Sinhala, and Sundanese}},
    author = {Keshan Sodimana and Knot Pipatsrisawat and Linne Ha and Martin Jansche and Oddur Kjartansson and Pasindu De Silva and Supheakmungkol Sarin},
    booktitle = {Proc. The 6th Intl. Workshop on Spoken Language Technologies for Under-Resourced Languages (SLTU)},
    year  = {2018},
    address = {Gurugram, India},
    month = aug,
    pages = {66--70},
    URL   = {http://dx.doi.org/10.21437/SLTU.2018-14}
}
```
