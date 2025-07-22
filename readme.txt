lisp
    オリジナル
    corvusskkの独自実装

succulents
    "https://supersabotentime.com/2185/"の"多肉植物ユーザー辞書A"をもとに作成
    作成手順 言語はvimscript gdefaultオプションを設定している
        g/\v\t[ワーラヤ マハナタサカアリミヒニチシキイルユムフヌッツスクウレエメィァェゥォャュョヘネテセケエヲロヨモホノトソコオンバダザガビヂジギヴブヅズグベデゼゲボドゾゴチパピプペポ]{-1,}\t/d "変換先が片仮名のものを削除
        g/科/d
        %s/\v\t(固有名詞|多肉植物A)// "不要な情報を削除
        %s/\t/ \// "SKK辞書の形にする
        %s/\//;[多肉]\// "スラッシュの前に';[多肉]'を挿入
        %s/;[多肉]//g "見出し語にも追加してしまうので それを消す
        %s/キリン/麒麟/ "'キリン'を'麒麟'に置換

zipcode
    "https://github.com/skk-dev/dict/raw/refs/heads/master/zipcode/SKK-JISYO.zipcode"より作成
    手順
        %s/\/$/;[郵]\//
