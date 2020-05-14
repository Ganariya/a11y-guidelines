.. _category-text:

テキスト
----------------------------

これらのガイドラインは、テキスト情報に関するものです。テキスト情報とは、大ざっぱにいえば文字情報ですが、文字情報を画像化して表示するものはこれらのガイドラインの対象ではありません。これについては、「画像化されたテキストに関するガイドライン」を参照してください。

.. _text-wording:

文言
~~~~

参考: :ref:`exp-text-wording` 

.. _gl-text-multiple-modality:

-  [MUST] 何かを説明する場合、色、形状、位置など特定の感覚を前提とした説明をするのはかまわないが、その他の表現も併用する。

   .. raw:: html

      <details>

   意図
      *  視覚障害者、色弱者がコンテンツを利用できるようにする。
   チェック内容
      *  .. todo:: SC 1.3.3のチェック内容検討
   チェック対象
      |visual|
   対応するWCAG 2.1の達成基準
      *  SC 1.3.3:

         *  |SC 1.3.3|
         *  |SC 1.3.3ja|

   .. raw:: html

      </details>

   .. _gl-text-heading-label:
-  [MUST] 主題又は目的を説明する見出し及びラベルを付ける。

   .. raw:: html

      <details>

   意図
      *  視覚障害者が、ページ内で目的のコンテンツを見つけやすくする。
   チェック内容
      *  見出し、画像やフォーム・コントロールに付くラベルは、内容を適切に示す文言になっている。
   チェック対象
      |visual|
   参考
      *  .. todo:: 見出しやラベルの文言について、適切/不適切な事例がたぶん必要
   対応するWCAG 2.1の達成基準
      *  SC 2.4.6:

         *  |SC 2.4.6|
         *  |SC 2.4.6ja|

   .. raw:: html

      </details>

.. _text-lang:

自然言語
~~~~~~~~~~~~

参考: :ref:`exp-text-lang` 

.. _gl-text-page-lang:

-  [MUST] html要素に適切にlang属性を指定する。

   .. raw:: html

      <details>

   意図
      *  音声/点字出力などが適切に行われるようにする。
   チェック内容
      *  日本語のページには、 ``<html lang="ja">`` の記述がある。
   チェック対象
      |markup|
   対応するWCAG 2.1の達成基準
      *  SC 3.1.1:

         *  |SC 3.1.1|
         *  |SC 3.1.1ja|

   .. raw:: html

      </details>

   .. _gl-text-phrase-lang:
-  [SHOULD] 段落単位など、比較的長いテキストの言語がhtml要素のlang属性で指定したものと異なる場合は、その部分に対して適切にlang属性を指定する。

   .. raw:: html

      <details>

   意図
      *  音声/点字出力などが適切に行われるようにする。
   チェック内容
      *  複数の言語が含まれているテキストについて、iOS VoiceOverのように多言語対応している読み上げ環境を用いて読み上げさせたとき、適切な言語の音声エンジンで読み上げられる。
   チェック対象
      |behavior| 、 |markup|
   対応するWCAG 2.1の達成基準
      *  SC 3.1.2:

         *  |SC 3.1.2|
         *  |SC 3.1.2ja|

   .. raw:: html

      </details>

.. _text-magnification:

テキスト表示の拡大
~~~~~~~~~~~~~~~~~~~~

参考: :ref:`exp-magnification` 

.. _gl-text-zoom:

-  [MUST] コンテンツや機能を損なうことなくブラウザーのズーム機能で200パーセントまで拡大できるようにする。

   .. raw:: html

      <details>

   意図
      *  ロービジョン者が、問題なくコンテンツを利用できるようにする。
   チェック内容
      *  200パーセントまで拡大しても、テキストの理解を妨げるようなレイアウト崩れが起こらない。
   チェック対象
      |visual| 、 |behavior|
   対応するWCAG 2.1の達成基準
      *  SC 1.4.4:

         *  |SC 1.4.4|
         *  |SC 1.4.4ja|

   .. raw:: html

      </details>

   .. _gl-text-zoom-reflow:
-  [SHOULD] 4倍に拡大表示したときでも、縦スクロールを前提としたコンテンツては横スクロールが、横スクロールを前提としたコンテンツでは縦スクロールが必要にならないようにする。

   .. raw:: html

      <details>

   意図
      *  ロービジョン者が、ズーム機能で拡大表示しても問題なくコンテンツを利用できるようにする。
   チェック内容
      *  4倍の拡大表示をしたときにも適切にリフローされ、読み取れない内容や利用できない機能がない。
   チェック対象
      |visual| 、 |behavior|
   対応するWCAG 2.1の達成基準
      *  SC 1.4.10:

         *  |SC 1.4.10|
         *  |SC 1.4.10ja|

   .. raw:: html

      </details>

.. _text-display:

テキストの表示
~~~~~~~~~~~~~~~~

.. _gl-text-customize:

-  [MUST] ユーザーがline-heightを1.5em以上、段落感の空白を2em以上、letter-spacingを0.12em以上に変更し、その他のプロパティーを一切変更していない状況において、コンテンツおよび機能に損失が生じないようにする。

   .. raw:: html

      <details>

   意図
      *  ロービジョン者が、問題なくコンテンツを利用できるようにする。
   チェック内容
      *  line-heightを1.5em以上、段落感の空白を2em以上、letter-spacingを0.12em以上に変更するユーザーCSSを適用しても、表示順序が変わる、文章を途中で読めなくなるなど、コンテンツおよび機能に損失が生じない。
   チェック対象
      |behavior|
   参考
      *  .. todo:: CSSの書き方、ユーザーCSSの適用方法などについて詳述してリンク
   対応するWCAG 2.1の達成基準
      *  SC 1.4.12:

         *  |SC 1.4.12|
         *  |SC 1.4.12ja|

   .. raw:: html

      </details>

   .. _gl-text-color-only:
-  [MUST] 文字色に何らかの意味を持たせている場合、書体など他の視覚的な要素も併せて用い、色が判別できなくてもその意味を理解できるようにする。

   .. raw:: html

      <details>

   意図
      *  視覚障害者、色弱者がコンテンツを利用できるようにする。
   チェック内容
      *  テキストはグレースケール表示でも意図が伝わるような文言になっている。
   チェック対象
      |visual|
   参考
      *  :ref:`exp-grayscale` 
   対応するWCAG 2.1の達成基準
      *  SC 1.4.1:

         *  |SC 1.4.1|
         *  |SC 1.4.1ja|

   .. raw:: html

      </details>

   .. _gl-text-contrast:

-  [MUST] 文字色と背景色に十分なコントラスト を確保する。

   -  テキストの文字サイズが22ポイント以上の場合: 3:1以上 ([SHOULD] 4.5:1以上)
   -  テキストの文字サイズが18ポイント以上で太字の場合: 3:1以上 ([SHOULD] 4.5:1以上)
   -  その他の場合: 4.5:1以上 ([SHOULD] 7:1以上)

   .. raw:: html

      <details>

   意図
      *  ロービジョン者が、コンテンツを利用できるようにする。
   チェック内容
      *  テキストは、文字色と背景色に十分なコントラストが確保されている。
   チェック対象
      |visual|
   参考
      *  :ref:`exp-contrast` 
   対応するWCAG 2.1の達成基準
      *  SC 1.4.3:

         *  |SC 1.4.3|
         *  |SC 1.4.3ja|

      *  SC 1.4.6:

         *  |SC 1.4.6|
         *  |SC 1.4.6ja|

   .. raw:: html

      </details>

.. todo:: explanations/text-display.rstを書き直してリンク。
