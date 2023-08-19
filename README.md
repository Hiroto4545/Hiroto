# 問い合わせ管理シート効率化

## 1 今回のコードでできること

失注した案件を自動で検出し、通知することができる。

## 2 実行方法

1. 各フォルダに移行
2. >ruby app.rb 

## 3 処理の流れ

処理の流れとしては、まずGASを使用しスプレッドシートの受注確度に変更があった場合、その日付をスプレッドシートに自動記入する。
rubyでスプレッドシートの情報を読み取り、受注確度が「G」かつ、その変更が１週間以内だった場合、その案件を失注とみなしchatworkへ通知する。

## 4 詳細

使用したシートはhttps://docs.google.com/spreadsheets/d/1aCE1AjyOofbz24X2G-nWcafXt87eEZYVejQ46YPyHxU
メッセージ内容は「案件失注のお知らせ　スプレッドシート:〇〇, シート:〇〇, 行: 〇〇」
本番情報にする際に変更すべきコードの箇所は「client_id,client_secret,spreadsheet_key,sheet_title,work_sheet[](行番号と列番号）,room_id」


