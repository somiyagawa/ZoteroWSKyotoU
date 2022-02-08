---
marp: true
theme: gaia
class: lead
header: "**UD入門WS 2022年2月11日**"
footer: "by **So Miyagawa**"
backgroundColor: 	
size: 16:9
paginate: true

style: |
    @import url(http://fonts.googleapis.com/earlyaccess/notosansjp.css);
    section.title {
        justify-content: center;
        text-align: center;
        font-family: 'Noto Sans JP', sans-serif;
    }
    body {
        font-family: 'Noto Sans JP', sans-serif;
    }
    h2 {
        color: orange;
        font-family: 'Noto Sans JP', sans-serif;
    }
      section {
        justify-content: center;
        text-align: left;
        font-family: 'Noto Sans JP', sans-serif;
    }
    
---
<!-- _class: title -->
# Universal Dependencies <br>入門ワークショップ

宮川 創
## So Miyagawa

京都大学 大学院文学研究科・文学部 助教
Twitter: @So_Miyagawa
miyagawa.so.36u@kyoto-u.jp
somiyagawa.com 
CC BY-SA 3.0
<!--
_color: #fffff9
-->
![bg brightness:0.2](https://upload.wikimedia.org/wikipedia/commons/b/b5/Universal_joint.gif)

---

## Universal Dependencies

*Universal Dependencies (UD)は、人間の異なる言語間で文法（品詞、形態素情報、統語依存関係）を**一貫して**アノテーションするためのフレームワークである。UDは、**300**人以上の貢献者が**100以上の言語**で**200近くのツリーバンク**を作成するオープンなコミュニティ活動である。*

![bg right:35% height:60%](https://universaldependencies.org/logos/logo-ud.png)
<!--
_footer: '文章は[UD公式サイト](https://universaldependencies.org/)から翻訳'
-->
---
## UDの目的
*UDは、言語類型論の観点から、多言語解析器の開発、通言語的学習、構文解析研究を促進することを目的に、多言語の通言語的一貫ツリーバンク注釈を開発しているプロジェクトである。*
<!--
_footer: '文章は[UD公式サイト](https://universaldependencies.org/introduction.html)から翻訳
'
-->


---
## UDの歴史
- *このアノテーションは、スタンフォード依存関係（de Marneffe et al., 2006, 2008, 2014）、Googleユニバーサル品詞タグ（Petrov et al 2012)そして、形態統語タグセットであるインターセット・インターリングア（Zeman 2008）の進化に基づいている.*
- *一般的な理念は、言語間で類似構文の一貫したアノテーションを容易にするために、普遍的なカテゴリとガイドラインの目録を提供し、必要な場合は言語固有の拡張を可能にすることである。*
<!--
_footer: '文章は[UD公式サイト](https://universaldependencies.org/introduction.html)から翻訳
'
-->


---
## 要するに

- UDは、全ての言語の統語・形態情報を同じ様に記述することによって、通言語的な分析を容易にする→言語類型論や歴史言語学、一般言語学に使える！
- また、多言語機械翻訳のデータとしても使える→民間企業からも多数参入（例：Google, リクルートetc.)
- 2013年、スタンフォード大学の依存文法プロジェクト ＋ Google ユニバーサル品詞タグ + プラハ・カレル大学のインターセット・インターリングア → Universal Dependencies成立

---
## UDの基礎知識

- 依存文法
- UPOS
- 依存関係
- CoNNL-U

<!--
_footer: 'Photo by Peo Hedin on Unsplash'
-->
![bg left:40% brightness:0.8](https://images.unsplash.com/photo-1595939572262-3666138363af?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80)


---
## 依存文法

- フランスのルシアン・テニエール(1893-1954)
- 文のなかの語の依存関係を軸に統語論を記述する
- 日本語では、係り結びを連想させる「係り受け」で定着
- 句構造文法や生成文法のように、語よりも大きな単位で、入れ子構造になる「句」を前提としない
- 句構造文法よりは情報量が少なくなるが、語順が自由な言語などどんな言語でも容易に対応できる
- 句構造文法にも変換可能


---

![bg 80%](https://upload.wikimedia.org/wikipedia/commons/0/0d/Wearetryingtounderstandthedifference_%282%29.jpg) 
<!--
_footer: 'Image by Tjo3ya on Wikimedia Commons under CC BY-SA 3.0'
-->
---

![bg 80%](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/The_house_at_the_end_of_the_street.jpg/640px-The_house_at_the_end_of_the_street.jpg)
<!--
_footer: 'Image by Tjo3ya on Wikimedia Commons under CC BY-SA 3.0'
-->
---

## UPOS (ユニバーサル品詞タグ)
- 全ての言語で同じ品詞タグを使う
- 言語個別のXPOSに対応させる
- NOUN = 名詞、VERB = 動詞、ADP = 側置詞・・・
- https://universaldependencies.org/u/pos/



---
## 依存関係 (Dependency Relations)

- 別名「係り受け関係」
- ある語と別の語はどちらが主要部でどちらが従属部か
- それら２つの語の関係はなにか？
- nsubj = 名詞主語、obj = 目的語、iobj = 間接目的語・・・
- https://universaldependencies.org/u/dep/index.html

---
## CoNNL-U形式

![height:180](https://miro.medium.com/max/1400/1*eU7KKpB1pKZOfY2aVnVwSw.png)
(https://miro.medium.com/max/1400/1*eU7KKpB1pKZOfY2aVnVwSw.png より)

- [他の例もみてみよう（UD公式ホームページ）](https://universaldependencies.org/format.html) 
- [日本語の例 (国語研の大村氏と浅原氏によるBCCWJのUD化)](https://irdb.nii.ac.jp/01129/0001535528)

---

## エディタ
[ツール一覧はこちら](https://universaldependencies.org/tools.html)
- ExcelやGoogle Spreadsheet
- [deplacy](https://github.com/KoichiYasuoka/deplacy) (おすすめ！）
- [Arborator Grew](https://arboratorgrew.elizia.net/)
- [VSCode](https://code.visualstudio.com/)
- [WebAnno](https://webanno.github.io/webanno/)
- [conllu.js](http://spyysalo.github.io/conllu.js/)
![bg right:50% 100%](https://universaldependencies.org/img/conllueditor_tree.png)


---
## UDPipeを体験してみよう

- UDPipeとは
    - プラハ・カレル大学が開発しているUD自動解析器（パーサー）
- GitHub上の多数の言語のUDツリーバンクを学習している
- UDPipe1, UDPipe2, UDPipe3
- 日本語のパーサーもある

クリック→ https://lindat.mff.cuni.cz/services/udpipe/

---

## deplacyを体験してみよう
- 京都大学の安岡孝一教授が作成
- 様々な可視化
- 使いやすいエディタ
- リクルートと国語研が開発したGiNZAなど、様々な学習済みモデルが使える

クリック→[deplacyによる日本語解析](https://colab.research.google.com/github/KoichiYasuoka/deplacy/blob/master/doc/ja.ipynb)


<!--
_footer: 'Photo from https://www.zinbun.kyoto-u.ac.jp/members/private/yasuoka.html'
-->
![bg right:35% brightness:1.2](https://www.zinbun.kyoto-u.ac.jp/images/members/32.YASUOKA-Koichi.jpg)