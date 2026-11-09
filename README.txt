地歴公民 作問アシスタント
PDFの切り抜き → 問題の編集 → Word出力 を、ブラウザの中だけで行うアプリです。


【安全性】
このアプリは、PDF・画像・文章・問題を外部のサーバーへ送信しません。
index.html に「同じ場所に置いたファイル以外とは通信しない」というブラウザ向けの設定（Content-Security-Policy）を書いてあるため、
それ以外への通信はブラウザ自身が止めます。
PDF表示（pdf.js）、文字認識OCR（Tesseract.js）、Word作成（docx）の部品も、すべて lib フォルダに同梱しています。
作業内容は、使っている端末のブラウザの中（IndexedDB）にだけ自動保存されます。


【GitHub Pages で公開する手順】（無料。誰でも開けるURLになります）
1　GitHub にログインし、右上の「＋」→「New repository」を押す。
2　Repository name に半角英数字で名前を付ける（例：sakumon）。「Public」を選び、「Create repository」を押す。
　　※無料プランで GitHub Pages を使うには Public が必要です。公開されるのはアプリのファイルだけで、
　　　先生方が開くPDFや作った問題は公開されません（各自のブラウザの中だけで処理されます）。
3　作成直後の画面にある「uploading an existing file」を押す。
4　このZIPを展開してできたフォルダを開き、その「中身」（index.html・lib フォルダ・README.txt）をまとめて選んで、
　　ブラウザの画面にドラッグ＆ドロップする。
　　※フォルダそのものではなく「中身」を入れてください。
　　※lib フォルダの中のフォルダ（lib/pdfjs、lib/tesseract など）がそのまま入ったことを、一覧で確認してください。
　　　Chrome または Edge でドラッグするとフォルダ構成が保たれます。
5　画面下の「Commit changes」を押す。
6　上のメニューの「Settings」→ 左の「Pages」→「Build and deployment」の Branch で「main」と「/(root)」を選び「Save」。
7　1〜2分待って同じ画面を再読み込みすると、上部に URL（https://ユーザー名.github.io/sakumon/）が出ます。
　　このURLを開けば使えます。他の先生にはこのURLを伝えるだけで使ってもらえます。


【使うときの注意】
・index.html をパソコン上でダブルクリックして開くと、ブラウザの制限でPDFが表示されません。必ず公開したURLから開いてください。
・PDF本体は保存されません。続きの作業をするときは、同じPDFをもう一度開いてください。
・別のPCで続けたいときは、画面右上の「作業ファイルを保存」で .json を保存し、別のPCで「作業ファイルを開く」を使います。
・ブラウザの閲覧履歴やサイトデータを消すと、自動保存された作業内容も消えます。大事な作業は「作業ファイルを保存」で控えを取ってください。
・Wordのフォントは「游明朝」がWindows・Macの両方で使えます。
・教科書・資料集の図版や文章を考査に使うときは、出典を明記してください。


【同梱ライブラリとライセンス】
pdf.js（Apache License 2.0）　lib/pdfjs/LICENSE.txt
docx（MIT License）　lib/docx-LICENSE.txt
Tesseract.js・tesseract.js-core（Apache License 2.0）　lib/tesseract/LICENSE.txt、lib/tesseract/core/LICENSE.txt
OCR用の言語データ（tessdata：Apache License 2.0）　lib/tesseract/lang
