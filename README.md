<h1>
  <a href="https://hkilang.github.io/TTS/"><img src="../../../TTS/raw/main/public/assets/favicon-256x256.png" width="84" align="left" /></a>
  <div lang="zh-HK">香港圍頭話及客家話文字轉語音</div>
  <div><sub>Hong Kong Waitau & Hakka Text-to-Speech</sub></div>
</h1>

<p>
  <div lang="zh-HK">本儲存庫包含<a href="https://hkilang.github.io/TTS/"><strong>香港圍頭話及客家話文字轉語音</strong></a>之預生成音訊檔案。當選擇輕巧模式時，朗讀器程式會從中選取音訊片段拼接，於程式內直接產生音訊。</div>
  <div>This repository contains the pre-generated audio files of the <a href="https://hkilang.github.io/TTS/"><strong>Hong Kong Waitau & Hakka Text-to-Speech</strong></a> reader. In lightweight mode, the TTS application generates audio by concatenating selected audio segments right inside the app.</div>
</p>

These files are created as follows:

* For each language (`waitau` and `hakka`):
  * For each voice (`male` and `female`):
    * For each character in the dictionary, an audio file is generated using [the model for offline inference](../../../TTS-models).
    * The generated files are then concatenated into a single file, `chars.bin`, and the corresponding pronunciation and the start offset for each audio file is saved into an offset table, `chars.csv`.
    * The same is performed for each word in the dictionary, producing the files `words.bin` (split into smaller chunks due to size limitations) and `words.csv`.

For how they are used by the main app, **refer to the [_Audio Generation_](../../../TTS#audio-generation) section** in the README of the TTS repo.
