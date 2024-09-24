+++
title = 'Ollama'
date = 2024-09-22T11:28:08+08:00
draft = false
+++

# Ollama: a response to some AI-related concerns?

Since ChatGPT came out, I've been following the news about LLMs and the exponentially increasing list of available models. While I recognise the potential and the technical achievement they represent, I am quite worried about what they mean for the future for several reasons:
- [Each query consumes a lot of resources](https://www.washingtonpost.com/technology/2024/09/18/energy-ai-use-electricity-water-data-centers/), which is definitely not helping with climate change.
- What do they mean with regards to the future of content? Are we going to be mostly presented AI generated stuff in the future?
- How ethical is the training of the different models? Does it use copyrighted content? How to ensure it does not?
- What's up with privacy when using server-side services like ChatGPT, Copilot etc which reuse user input to further train the models?

One possible lead to address some of these concerns by running smaller models that are designed to be run on a single machine, and I've been recently looking at [Ollama](https://ollama.com/) for this.

Ollama allows you to run models locally, including Llama 3.1, Phi 3, Mistral, Gemma 2. These models are usually lighter, less "smart" versions of what you'd get from the companies backing them using their APIs. However they're designed to run on a single machine (I use them on my MacBook), but they still perform very well. For example, I am here using mistral-nemo to help me with my Mandardin learning and asking it to give me 3 examples using a specific grammar pattern:

```
>>> 給我三個例句用「只要」
 1. 只要你努力，就一定會成功。
   (Zìyán wǒ nǎlì, jiù yīdìng huì chénggōng.)
   Translation: As long as you try, you will definitely succeed.
2. 只要天氣好，我們就去公園玩。
   (Zìyán tiānqì hǎo, wǒmen jiù qù gōngyuán wán.)
   Translation: We'll go to the park if the weather is good.
3. 只要有時間，我就會來幫忙。
   (Zìyán yǒu shíjiàn, wǒ jiù huì lái bāngwán.)
   Translation: Whenever I have time, I'll come and help out.

Here are three examples using "只要":

* 只要你努力，就一定會成功。
* 只要天氣好，我們就去公園玩。
* 只要有時間，我就會來幫忙。
```

For coding related work, it is also possible to replace Github Copilot with Ollama and [Continue](https://www.continue.dev/), which makes it free and eliminates privacy concerns, especially in an enterprise environment.

Running local models instead of using third party APIs can help address some of the concerns raised by LLMs: privacy issues, by not feeding them back to train the models on your data, and environmental impact, by using available local processing power instead of cloud resources. However, some others are not covered, specifically the impact of training, the infamous hallucinations, which we probably will never completely get rid of, and the ethical and future of content concerns, which are inherent to the use of LLMs in the first place. Seems like we'll still need humans around for a while!