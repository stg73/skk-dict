文字入力を強化するためのSKK辞書群

各辞書の説明 仕様は"specification.txt"

bamboo-copter.skk
    竹とんぼ

idiom.skk
    慣用句
    文脈を加味できないというSKKの欠点を補うこともできる

line-drawing-characters.skk
    罫線素片

lisp.skk
    corvusskk用のプログラム実行変換

succulents
    多肉植物に関する辞書群

    "term.skk"以外は"https://supersabotentime.com/12578/"の"多肉植物ユーザー辞書A"("https://supersabotentime.com/wp/wp-content/uploads/2022/02/2bbe09974e83aa8860c20437bee1b7d8.txt")をもとに作られている
    作成手順 vimscriptで書かれている "gdefault"を設定している
        g/\v\t[ワーラヤ マハナタサカアリミヒニチシキイルユムフヌッツスクウレエメィァェゥォャュョヘネテセケエヲロヨモホノトソコオンバダザガビヂジギヴブヅズグベデゼゲボドゾゴチパピプペポ]{-1,}\t/d " 変換候補が片仮名のものを削除
        g/科/d " 多肉植物の辞書に載せるようなものでもないので削除
        %s/\v\t(固有名詞|多肉植物A)// " 不要な情報を削除
        %s/\t/ \// | %s/$/\// " SKK辞書の形にする
        %s/\v(\/$)@=/;[多肉]/ " '[多肉]'の注釈を挿入
        %s/キリン/麒麟/ " 'キリン'を漢字に

    succulents/genus-name.skk
        属名

    succulents/japanese-name.skk
        和名

    succulents/scientific-name.skk
        学名

    succulents/term.skk
        用語

wrong.skk
    "はこびる"などの誤りを補正し 正しい形を示してくれる辞書 たとえば "はこびr /蔓延;[誤]はびこr/"
    昔"ゆういつ"が変換できなくて困ったことがあり そういう時に変換したうえで正しい形を示してくれる辞書が欲しかった
