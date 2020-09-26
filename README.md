
**Moji4J** is an open source Java library to converts between Japanese Hiragana, Katakana, and Romaji scripts.

## Romaji and Kana Conversion

```java
MojiConverter converter = new MojiConverter();

converter.convertRomajiToHiragana("Hiragana"); // ひらがな
converter.convertRomajiToKatakana("Katakana"); // カタカナ
converter.convertKanaToRomaji("ひらがな"); // hiragana
converter.convertKanaToRomaji("カタカナ"); // katakana
```

## Romaji, Kana, and Kanji Detection

```java
MojiDetector detector = new MojiDetector();

detector.hasKanji("まっ暗"); // true
detector.hasKanji("まっしろ"); // false
detector.hasKana("ウソ付き"); // true
detector.hasKana("東京"); // false
detector.hasRomaji("モデル XYZ"); // true
detector.hasRomaji("フルーツ"); // false
```

## Romanization Convention

The romanization system adopted by this library is loosely based on the [modern Hepburn system][1], with adjustments for cases that might causes ambiguity during conversion.

| Cases           | Romaji    | Kana      
|-----------------|-----------|-----------
| Long vowels     | sentaa    | センター
|                 | ookayama  | おおかやま
| *o+u* vowels    | toukyou   | とうきょう
|                 | ousama    | おうさま
| Long consonants | kekka     | けっか
|                 | kasetto   | カセット
|                 | kotchi    | こっち
| Syllabic *n*    | gunma     | ぐんま
|                 | kan'i     | かんい
|                 | shin'you  | しんよう
| Particles       | he        | へ
|                 | wo        | を
| Others          | dzu       | づ

## Acknowledgement

This software includes the work that is distributed in the Apache License 2.0.

### [andree-surya/moji4j][2]

    © Copyright 2016 Andree Surya

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[1]: https://en.wikipedia.org/wiki/Hepburn_romanization
[2]: https://github.com/andree-surya/moji4j
