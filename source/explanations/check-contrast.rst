.. _exp-check-contrast:

コントラスト比のチェック方法
------------------------------

ロービジョン者でもコンテンツを知覚できるよう、テキストやUIコンポーネントにはそれぞれコントラスト比の基準を満たす色が使われることが求められます。

実際のWebページから色のコントラスト比が不足している場所を発見するには `axe <https://www.deque.com/axe/>`_ のようなチェックツールを使用し、
具体的な色同士のコントラスト比の計算には `WebAIM: Contrast Checker <https://webaim.org/resources/contrastchecker/>`_ のような計算ツールを使用します。

アクセシビリティー・チェックツールの使用
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

`axe <https://www.deque.com/axe/>`_ を使用すると、Webページ全体から（コントラスト比以外にも）アクセシビリティー上の問題のある場所を発見することができます。

Google Chromeの場合、開発者ツールの Audits タブに Lighthouse が搭載されていますが、これで採点できるもののうち、 Accessbility については axe が使用されています。
また、 `axe の Google Chrome 拡張 <https://chrome.google.com/webstore/detail/axe-web-accessibility-tes/lhdoppojpmngadmnindnejefpokejbdd>`_ を使用すると、結果を日本語で読むこともできます。


コントラスト比の計算ツールの使用
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

コントラスト比の計算式は非常に複雑であるため、 `WebAIM: Contrast Checker <https://webaim.org/resources/contrastchecker/>`_ のような計算ツールを使用することが一般的です。
`contrast.app <https://usecontrast.com/>`_ のように、インストールして常駐させるタイプのチェッカーも存在します。

このようなコントラスト比計算ツールを使用する場合は以下の点に注意が必要です。

*  コントラスト比の計算ツールによって小数点以下の丸め方に差異があり、計算結果がバラつくことがある。

   -  計算結果は目安として、コントラスト比に余裕のある色を選ぶのが望ましい。

*  カラーピッカーを使用する場合、macOSではディスプレイのカラープロファイルの影響を受けることがあるため、これを防ぐ必要がある。

   -  `macOSのカラープロファイル設定 <https://support.apple.com/ja-jp/guide/mac-help/mchlf3ddc60d/mac>`_ で、「このディスプレイのプロファイルのみを表示」のチェックを外してから ``SRGB IEC61966-2.1`` を選択。
   -  SketchではPreferences➝General➝Color Profileで「SRGB IEC61966-2.1」を選択。

      -  上記はデフォルト設定なので、既存のドキュメントのカラープロファイルは異なったままになっている可能性があります。ファイルのカラープロファイルを変えたい場合は :menuselection:`File --> Change Color Profile` から変更します。
      -  参考： `Sketch : Color Management <https://www.sketch.com/support/troubleshooting/color-management/>`_

   -  Adobe XDはOSの設定を引き継ぐので、カラープロファイルの設定を変更した場合は再起動。

参考： :ref:`exp-contrast`

関連ガイドライン
~~~~~~~~~~~~~~~~

*  アイコン： :ref:`gl-icon-contrast`
*  画像： :ref:`gl-image-adjacent-contrast`
*  画像： :ref:`gl-image-text-contrast`
*  画像化されたテキスト： :ref:`gl-iot-adjacent-contrast`
*  画像化されたテキスト： :ref:`gl-iot-text-contrast`
*  テキスト： :ref:`gl-text-contrast`
