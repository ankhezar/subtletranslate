# Third-Party Notices & Attributions

**Subtle** (`SubtleTranslate.app`, App Store listing **`Subtle — Instant Translator`**) incorporates or interoperates with the following open-source software components and pre-trained machine-learning models:

---

## 1. Meta `fastText` Pre-Trained Language Identification Model (`lid.176.ftz`)

- **Source:** https://fasttext.cc/docs/en/language-identification.html (`https://dl.fbaipublicfiles.com/fasttext/supervised-models/lid.176.ftz`)
- **License:** [Creative Commons Attribution-ShareAlike 3.0 Unported (`CC BY-SA 3.0`)](https://creativecommons.org/licenses/by-sa/3.0/)
- **Modifications:** Bundled **unmodified** (`Resources/LanguageID/lid.176.ftz`, `938,013` bytes, SHA-256 `7e69ec5451bc261cc7844e49e4792a85d7f09c06789ec800fc4a44aec362764e`) as a standalone data asset read by Subtle's pure-Swift `FastTextLIDClassifier`. No derivative model weights are distributed.
- **Citations:**
  - Armand Joulin, Edouard Grave, Piotr Bojanowski, Tomas Mikolov, *"Bag of Tricks for Efficient Text Classification"*, EACL 2017 (`arXiv:1607.01759`).
  - Armand Joulin, Edouard Grave, Piotr Bojanowski, Matthijs Douze, Hérve Jégou, Tomas Mikolov, *"FastText.zip: Compressing text classification models"*, 2016 (`arXiv:1612.03651`).

---

## 2. Google `TranslateGemma` (Optional On-Demand Offline AI Packs)

- **Models:** `translategemma-4b-it` (`Q4_K_M` GGUF, ~2.5 GB) and `translategemma-12b-it` (`Q4_K_M` GGUF, ~7.3 GB) — not bundled inside `SubtleTranslate.app`; downloaded strictly on explicit user request into `~/Library/Application Support/SubtleTranslate/Models/`.
- **Terms & Notice:** Gemma is provided under and subject to the **Gemma Terms of Use** found at https://ai.google.dev/gemma/terms. Users downloading and using optional TranslateGemma offline model packs agree to comply with the Gemma Terms of Use and Prohibited Use Policy (https://ai.google.dev/gemma/prohibited_use_policy).

---

## 3. `llama.cpp` (`SubtleTranslateInferenceHelper`)

- **Source:** https://github.com/ggml-org/llama.cpp
- **Copyright:** Copyright (c) 2023–2026 Georgi Gerganov and contributors
- **License:** MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## 4. Supertone `Supertonic-3` & `FluidInference/supertonic-3-coreml` (Optional On-Demand Neural Voice Pack)

- **Models:** `supertonic-3-coreml` (`v2`, ~130 MB across 4 Core ML modules + Unicode indexer & speaker style presets, converted from `Supertone/supertonic-3` v1.7.3) — not bundled inside `SubtleTranslate.app`; downloaded strictly on explicit user request into `~/Library/Application Support/SubtleTranslate/Models/supertonic-3-coreml-v2/`.
- **Model Weights License:** **BigScience Open RAIL-M License** (dated August 18, 2022 — https://huggingface.co/FluidInference/supertonic-3-coreml/blob/2b5b939dfa1bca362c5212dcafeb8aadde90b1bc/LICENSE). Users downloading and operating the optional Supertonic-3 voice pack agree not to use the model or its outputs for any restricted harmful, deceptive, or illegal use cases listed in Attachment A of the BigScience Open RAIL-M License (including unlawful discrimination, impersonation/deception without disclosure, defamation, medical/legal advice, or exploitation of minors).
- **Conversion & Pipeline Reference:** `FluidInference/FluidAudio` (https://github.com/FluidInference/FluidAudio), Copyright (c) Fluid Inference contributors, licensed under the **Apache License, Version 2.0** (http://www.apache.org/licenses/LICENSE-2.0); upstream reference code by Supertone Inc. (https://github.com/supertone-inc/supertonic), licensed under the **MIT License**.

---

## 5. `Sparkle 2` (Standalone Direct-Download Edition Only)

- **Source:** https://github.com/sparkle-project/Sparkle (`https://sparkle-project.org`)
- **Copyright:** Copyright (c) 2006–2026 Andy Matuschak and Sparkle Project contributors
- **Scope:** Included strictly in the Standalone Direct-Download edition; completely excluded from Mac App Store builds.
- **License:** MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
