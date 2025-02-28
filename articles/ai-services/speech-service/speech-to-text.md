---
title: Speech to text overview - Speech service
titleSuffix: Azure AI services
description: Get an overview of the benefits and capabilities of the speech to text feature of the Speech service.
author: eric-urban
manager: nitinme
ms.service: azure-ai-speech
ms.topic: overview
ms.date: 5/21/2024
ms.author: eur
---

# What is speech to text?

In this overview, you learn about the benefits and capabilities of the speech to text feature of the Speech service, which is part of Azure AI services. Speech to text can be used for [real-time](#real-time-speech-to-text), [batch transcription](#batch-transcription-api), or [fast transcription](./fast-transcription-create.md) of audio streams into text. 

> [!NOTE]
> To compare pricing of [real-time](#real-time-speech-to-text), [batch transcription](#batch-transcription-api), and [fast transcription](./fast-transcription-create.md), see [Speech service pricing](https://azure.microsoft.com/pricing/details/cognitive-services/speech-services/). 

For a full list of available speech to text languages, see [Language and voice support](language-support.md?tabs=stt).

## Real-time speech to text

With real-time speech to text, the audio is transcribed as speech is recognized from a microphone or file. Use real-time speech to text for applications that need to transcribe audio in real-time such as:
- Transcriptions, captions, or subtitles for live meetings
- [Diarization](get-started-stt-diarization.md)
- [Pronunciation assessment](how-to-pronunciation-assessment.md)
- Contact center agents assist
- Dictation
- Voice agents

Real-time speech to text is available via the [Speech SDK](speech-sdk.md) and the [Speech CLI](spx-overview.md). 

## Fast transcription (Preview)

Fast transcription API is used to transcribe audio files with returning results synchronously and much faster than real-time audio. Use fast transcription in the scenarios that you need the transcript of an audio recording as quickly as possible with predictable latency, such as: 

- Quick audio or video transcription, subtitles, and edit. 
- Video translation  

> [!NOTE]
> Fast transcription API is only available via the speech to text REST API version 2024-05-15-preview and later. 

To get started with fast transcription, see [use the fast transcription API (preview)](fast-transcription-create.md).

## Batch transcription API

[Batch transcription](batch-transcription.md) is used to transcribe a large amount of audio in storage. You can point to audio files with a shared access signature (SAS) URI and asynchronously receive transcription results. Use batch transcription for applications that need to transcribe audio in bulk such as:
- Transcriptions, captions, or subtitles for prerecorded audio
- Contact center post-call analytics
- Diarization

Batch transcription is available via:
- [Speech to text REST API](rest-speech-to-text.md): To get started, see [How to use batch transcription](batch-transcription.md) and [Batch transcription samples (REST)](https://github.com/Azure-Samples/cognitive-services-speech-sdk/tree/master/samples/batch).
- The [Speech CLI](spx-overview.md) supports both real-time and batch transcription. For Speech CLI help with batch transcriptions, run the following command:
    ```azurecli-interactive
    spx help batch transcription
    ```

## Custom speech

With [custom speech](./custom-speech-overview.md), you can evaluate and improve the accuracy of speech recognition for your applications and products. A custom speech model can be used for [real-time speech to text](speech-to-text.md), [speech translation](speech-translation.md), and [batch transcription](batch-transcription.md).

> [!TIP]
> A [hosted deployment endpoint](how-to-custom-speech-deploy-model.md) isn't required to use custom speech with the [Batch transcription API](batch-transcription.md). You can conserve resources if the [custom speech model](how-to-custom-speech-train-model.md) is only used for batch transcription. For more information, see [Speech service pricing](https://azure.microsoft.com/pricing/details/cognitive-services/speech-services/).

Out of the box, speech recognition utilizes a Universal Language Model as a base model that is trained with Microsoft-owned data and reflects commonly used spoken language. The base model is pretrained with dialects and phonetics representing various common domains. When you make a speech recognition request, the most recent base model for each [supported language](language-support.md?tabs=stt) is used by default. The base model works well in most speech recognition scenarios.

A custom model can be used to augment the base model to improve recognition of domain-specific vocabulary specific to the application by providing text data to train the model. It can also be used to improve recognition based for the specific audio conditions of the application by providing audio data with reference transcriptions. For more information, see [custom speech](./custom-speech-overview.md) and [Speech to text REST API](rest-speech-to-text.md).

Customization options vary by language or locale. To verify support, see [Language and voice support for the Speech service](./language-support.md?tabs=stt).

## Responsible AI 

An AI system includes not only the technology, but also the people who use it, the people who are affected by it, and the environment in which it's deployed. Read the transparency notes to learn about responsible AI use and deployment in your systems. 

* [Transparency note and use cases](/legal/cognitive-services/speech-service/speech-to-text/transparency-note?context=/azure/ai-services/speech-service/context/context)
* [Characteristics and limitations](/legal/cognitive-services/speech-service/speech-to-text/characteristics-and-limitations?context=/azure/ai-services/speech-service/context/context)
* [Integration and responsible use](/legal/cognitive-services/speech-service/speech-to-text/guidance-integration-responsible-use?context=/azure/ai-services/speech-service/context/context)
* [Data, privacy, and security](/legal/cognitive-services/speech-service/speech-to-text/data-privacy-security?context=/azure/ai-services/speech-service/context/context)

## Next steps

- [Get started with speech to text](get-started-speech-to-text.md)
- [Create a batch transcription](batch-transcription-create.md)
