<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang xml:lang>
<head>
  <meta charset="utf-8" />
  <meta name="generator" content="pandoc" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes" />
  <title>output</title>
  <style>
    code{white-space: pre-wrap;}
    span.smallcaps{font-variant: small-caps;}
    span.underline{text-decoration: underline;}
    div.column{display: inline-block; vertical-align: top; width: 50%;}
    div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
    ul.task-list{list-style: none;}
  </style>
  <!--[if lt IE 9]>
    <script src="//cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv-printshiv.min.js"></script>
  <![endif]-->
</head>
<body>
<ul>
<li>ESS（JNJADMIN）</li>
<li>data user bên GENE
<ul>
<li>基本情報</li>
<li>発令情報
<ul>
<li>tạo 資格, 前役職, 前前役職
<ul>
<li>休退職区分 = 0 hoặc 1</li>
</ul></li>
</ul></li>
<li>拡張2:1320 管理区分</li>
<li>拡張2:1270 資格取得歴
<ul>
<li>tạo 前資格, 前前資格</li>
</ul></li>
<li>拡張2:1020 非発令情報</li>
<li>拡張2:1280 考課コース情報
<ul>
<li>tạo cho user cần đánh giá
<ul>
<li>dành cho loại đánh giá 一般用 (không phải 参与, 参事, 専門)
<ul>
<li>tham chiếu đến KK考課項目マスタ.職務区分コード</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li>人事考課
<ul>
<li>I. Thực hiện 準備 và thiết lập route
<ul>
<li><ol type="1">
<li>Thực hiện 準備 và 発令上組織 メニュー　＞　考課　＞ 人事考課　＞　人事考課（人事部） 期間：　　2024/04 ~ 2025/03 対象考課年月日：2024/12/01</li>
</ol>
<ul>
<li>１．準備処理
<ul>
<li>「準備する」ボタンを押す
<ul>
<li>Xác nhận hiển thị　資格_管理区分 từ　2．→7. (List danh sách 資格_管理区分 cần xác nhận)</li>
</ul></li>
<li>「確認する」ボタンを押す
<ul>
<li>Xác nhận kết quả　準備</li>
</ul></li>
</ul></li>
<li>２．人事考課ルート設定 「設定する」ボタンを押す
<ul>
<li>１．発令上組織設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="1">
<li>Thiết lập lại danh sách đối tượng đánh giá dựa trên soshiki メニュー　＞考課　＞　人事部　＞　ルート取込</li>
</ol>
<ul>
<li>発令上組織ルート取込CSVファイル準備
<ul>
<li>Tạo CSV import để loại bớt soshiki ra khỏi mục tiêu đánh giá
<ul>
<li>Thiết lập cột 処理フラグ＝D ở mỗi dòng csv</li>
</ul></li>
</ul></li>
<li>取込処理
<ul>
<li>対象　　　　：人事考課　　　　　ルート種類　　：発令上組資格／等級区分：。。。
<ul>
<li>「ファイル取込」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="3" type="1">
<li>Hoàn tất route settei メニュー　＞　考課　＞ 人事考課　＞　人事考課（人事部） 期間：　　2024/04 ~ 2025/03 対象考課年月日：2024/12/01</li>
</ol>
<ul>
<li>２．人事考課ルート設定 「設定する」ボタンを押す
<ul>
<li>２．役職及び人事担当関連設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
<li>３．非発令・被考課者設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
<li>「確認・修正」ボタンを押す
<ul>
<li>Xác nhận danh sách 社員対象 tương ứng với mỗi cặp 資格_管理区分
<ul>
<li>採用区分＝1，3：３年目以降</li>
<li>採用区分＝2，＞90：２年目以降</li>
<li>Đối với 社員 loại 管理区分：400 ⇒ 管理区分名称：一般職➞基幹職</li>
<li>Đối với 嘱託員 loại 管理区分：400 ⇒ 管理区分名称：一般職</li>
</ul></li>
</ul></li>
</ul></li>
<li>４．ルート確定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="I">
<li>Thực hiện đánh giá</li>
</ol>
<ul>
<li><ol type="1">
<li>Bắt đầu đánh giá メニュー　＞　考課　＞　人事考課　＞　人事考課（人事部） 期間：　　2024/04 ~ 2025/03 対象考課年月日：2024/12/01</li>
</ol>
<ul>
<li>３．人事考課実行
<ul>
<li>【実行する」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="1">
<li>Đánh giá lần 1 メニュー　＞　考課　＞　人事考課　＞　人事考課（第一考課者）</li>
</ol>
<ul>
<li>Ｖới mỗi loại 資格：　　　　　「考課開始」ボタンを押す
<ul>
<li>Tiến hành đánh giá cho từng shain S級社員_基幹職 và 嘱託員（F級社員）_一般職
<ul>
<li>Xuất CSV
<ul>
<li>Đối với 社員 loại 管理区分：400 ➞ 管理区分名称：一般職</li>
</ul></li>
<li>「考課終了」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="3" type="1">
<li>Đánh giá lần 2 trở đi メニュー　＞　考課　＞　人事考課　＞　人事考課（第二考課以降）</li>
</ol>
<ul>
<li>Đánh giá với mỗi loại 資格 tới hết JNJADMIN：　　　　　「考課開始」ボタンを押す
<ul>
<li>Tiến hành đánh giá cho từng shain S級社員_基幹職 và 嘱託員（F級社員）_一般職
<ul>
<li>Xuất CSV
<ul>
<li>Đối với 社員 loại 管理区分：400 ➞ 管理区分名称：一般職</li>
</ul></li>
<li>「考課終了」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li>III．Hoàn tất đánh giá
<ul>
<li>メニュー　＞　考課　＞　人事考課　＞　人事考課（人事部） 期間：　　2024/04 ~ 2025/03 対象考課年月日：2024/12/01
<ul>
<li>4．人事考課締め
<ul>
<li>締めを行う cho từng nhóm S級社員_基幹職 và 嘱託員（F級社員）_一般職
<ul>
<li>Kiểm tra ở GENE</li>
</ul></li>
<li>Kiểm tra kết quả ở mục 5．人事考課締め結果</li>
</ul></li>
<li>6．人事考課結果ダウンロード
<ul>
<li>【ダウンロード」ボタンを押す</li>
</ul></li>
<li>7．人事考課結果公開切替</li>
</ul></li>
</ul></li>
</ul></li>
<li>昇格推薦
<ul>
<li>I. Thực hiện 準備 và thiết lập route
<ul>
<li><ol type="1">
<li>Thực hiện 準備 và 発令上組織 メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（人事部） 昇格年：2024 、対象考課年月日：　2023/12/01</li>
</ol>
<ul>
<li>１．準備処理
<ul>
<li>「準備する」ボタンを押す
<ul>
<li>Xác nhận hiển thị　資格_管理区分 （E,S,F,J)職社員_基幹職）từ　2．→７．</li>
</ul></li>
<li>「確認する」ボタンを押す
<ul>
<li>Xác nhận kết quả　準備</li>
</ul></li>
</ul></li>
<li>２．昇格推薦ルート設定 「設定する」ボタンを押す
<ul>
<li>１．発令上組織設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
<li>２．役職及び人事担当関連設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
<li>３．非発令・被考課者設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="1">
<li>Thiết lập lại danh sách đối tượng đánh giá dựa trên soshiki メニュー　＞考課　＞　人事部　＞　ルート取込</li>
</ol>
<ul>
<li>取込処理
<ul>
<li>対象　　　　：昇格推薦　　　　　ルート種類　　：発令上組資格／等級区分：。。。
<ul>
<li>「ファイル取込」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="3" type="1">
<li>Hoàn tất route settei メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（人事部） 昇格年：2024 、対象考課年月日：　2024/12/01</li>
</ol>
<ul>
<li>２．昇格推薦ルート設定 「設定する」ボタンを押す
<ul>
<li>２．役職及び人事担当関連設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
<li>３．非発令・被考課者設定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
<li>４．ルート確定
<ul>
<li>「一括設定」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình 運用ログ</li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="I">
<li>Thực hiện đánh giá</li>
</ol>
<ul>
<li><ol type="1">
<li>Bắt đầu đánh giá メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（人事部） 昇格年：2024 、対象考課年月日：　2024/12/01</li>
</ol>
<ul>
<li>３．昇格推薦実行
<ul>
<li>【実行する」ボタンを押す
<ul>
<li>Kiểm tra kết quả ở màn hình</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="2" type="1">
<li>Đánh giá lần 1 メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（第一考課者）</li>
</ol>
<ul>
<li>Ｖới mỗi loại 資格：　　　　　「考課開始」ボタンを押す
<ul>
<li>Tiến hành đánh giá cho từng shain S級社員_基幹職
<ul>
<li>Xuất CSV
<ul>
<li>Đối với 社員 loại 管理区分：400 ➞ 管理区分名称：一般職</li>
</ul></li>
<li>「考課終了」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="3" type="1">
<li>Đánh giá lần 2 trở đi メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（第二考課以降）</li>
</ol>
<ul>
<li>Đánh giá mỗi loại 資格 tới hết JNJADMIN：　　　　　「考課開始」ボタンを押す
<ul>
<li>Tiến hành đánh giá cho từng shain S級社員_基幹職
<ul>
<li>Xuất CSV
<ul>
<li>Đối với 社員 loại 管理区分：400 ➞ 管理区分名称：一般職</li>
</ul></li>
<li>「考課終了」ボタンを押す</li>
</ul></li>
</ul></li>
</ul></li>
<li><ol start="4" type="1">
<li>Thực hiện 再推薦 メニュー　＞　考課　＞　人事部　＞　再推薦</li>
</ol></li>
</ul></li>
<li>III．Hoàn tất đánh giá
<ul>
<li>メニュー　＞　考課　＞　昇格推薦　＞　昇格推薦（人事部） 期間：　　2024/04 ~ 2025/03 対象考課年月日：2024/12/01
<ul>
<li>4．昇格推薦締め
<ul>
<li>締めを行う cho nhóm S級社員_基幹職
<ul>
<li>Kiểm tra ở GENE</li>
</ul></li>
<li>Kiểm tra kết quả ở mục 5．昇格推薦締め結果</li>
</ul></li>
<li>6．昇格推薦結果ダウンロード
<ul>
<li>【ダウンロード」ボタンを押す</li>
</ul></li>
<li>7．昇格推薦結果公開切替</li>
</ul></li>
</ul></li>
</ul></li>
</ul>
</body>
</html>
