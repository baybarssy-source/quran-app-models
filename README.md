# quran-app-models

Speech-recognition models used by the Quran app's recitation (tasmee') feature.
Files are converted, quantized and **encrypted for the app**; they are not usable on their own.

| Release | File | Source model | License |
|---|---|---|---|
| `iqra-v1` | `iqra-v1.qmdl` | [IqraEval/Iqra_wav2vec2_base](https://huggingface.co/IqraEval/Iqra_wav2vec2_base) on [facebook/wav2vec2-base-960h](https://huggingface.co/facebook/wav2vec2-base-960h) | Apache-2.0 |

## Attribution

- **Iqra'Eval** baseline (wav2vec2-base + BiLSTM CTC phoneme recognizer for Qur'anic recitation) —
  El Kheir et al., *Towards a Unified Benchmark for Arabic Pronunciation Assessment: Qur'anic Recitation as Case Study*, Interspeech 2025. Apache-2.0.
- **wav2vec 2.0** base, fine-tuned on LibriSpeech 960h — Meta AI. Apache-2.0.

Modifications: the upper 4 transformer layers were removed (their layer weights sum to 7.4%),
the model was exported to ONNX and dynamically quantized to int8, then compressed and encrypted.

---

نماذج التعرّف على الكلام لميزة التسميع في تطبيق القرآن الكريم. الملفّات محوّلة ومكمَّمة **ومشفّرة للتطبيق**، فلا تُستعمل خارجه.
