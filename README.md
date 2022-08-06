# Indonesian TTS

Indonesian TTS using Coqui TTS. Models are available in [Releases](https://github.com/Wikidepia/indonesian-tts/releases/) tab.

**DO NOT USE FOR COMMERCIAL PURPOSES!**

## Model changelog

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

## Data

- [Indonesian Azure TTS](https://depia.wiki/files/azure-tts.tar)
