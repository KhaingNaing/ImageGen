# ImageGen

Recently Google and Elon launched two powerful image generators: [IMAGEN3](https://deepmind.google/technologies/imagen-3/) and [GROK2](https://x.ai/). Both are capable of generating hyper realistic images with realistic texts. But none of them is open source. 

## FLUX.1 from Black Forest labs
In this repo we will try out [FLUX.1](https://blackforestlabs.ai/) from black forest labs. A strong image generation model that can generate realistic images and is open source. It is also the underlying model that powers GROK's images.
There are three different FLUX models. 

| Name | HuggingFace repo | License | 
| ---- | ---- | ---- | 
| `FLUX.1 [schnell]` | https://huggingface.co/black-forest-labs/FLUX.1-schnell | [apache-2.0](https://huggingface.co/datasets/choosealicense/licenses/blob/main/markdown/apache-2.0.md) | 
| `FLUX.1 [dev]` | https://huggingface.co/black-forest-labs/FLUX.1-dev | [FLUX.1 [dev] Non-Commercial License](https://huggingface.co/black-forest-labs/FLUX.1-dev/blob/main/LICENSE.md) | 
| `FLUX.1 [pro]` | Only available in their [API](https://fal.ai/models/fal-ai/flux-pro) |  | 

> ⚠️ **Warning:** Please refer to the license for proper model usage.

1. Schnell is the smallest model and can be used commercially.
2. The Dev model is available for experimentation but cannot be used commercially.
3. The Pro model is accessible via the Black Forest Lab API.

## To run huggingface dev model:

Replace the `prompt` in `huggingface.py` to product your desired image. Then run the command:
```
python3 huggingface.py
```

## To fine-tune your own model:

Below is a few open source projects that make fine-tunning FLUX easier:
  -  [SimpleTuner](https://github.com/bghira/SimpleTuner)
  - [x-flux](https://github.com/XLabs-AI/x-flux)

### To train your own LORA:
1. Need Data like a folder of images with corresponding json file that contain a caption for that image 
    ```
    {
        "caption": "a homeless cat holding a sign that says hi mom"
    }
    ```
2. From there we can fine tune hyperparameters then start training our own model with a signal command (More detailed on x-flux repo)

## To generate own imaginary friend 

- [ ] Build a data set of about 20 images and their corresponsind captions
- [ ] Train a LORA based on FLUX
- [ ] Produce voice using tool like [11Labs](https://elevenlabs.io/)
- [ ] Using tool like [PIKA Lab](https://pika.art/home) to generate video in lip sync mode to match the voice 

Congrats! Your loneliness is officially cured... or at least it's taken a vacation!



