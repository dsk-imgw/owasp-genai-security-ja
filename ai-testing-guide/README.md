# AI Testing Guide

- 原典は、[OWASP AI Testing Guide](https://github.com/OWASP/www-project-ai-testing-guide) の v1.0 で、当然英語のみ対応です。
- 原典への準拠性と日本語化の関係は以下のとおり。
  - 1_Intrduction → 原文の md ファイルを書式そのままに日本語化。
  - 2_Threat Modeling →（同上）
  - 3_AI TestingGuide Framework →（同上）
  - 3.x_TestingMethod →【2026/2/5 時点で作成中】
    - 項目とペイロードは、原文からそのまま引用しつつ、俯瞰性向上のために Excel 形式で一覧化しています。
    - ペイロード（英語）と判定基準は、上記 [OWASP AI Testing Guide](https://github.com/OWASP/www-project-ai-testing-guide) のものをベースとしているものの、一部は私の独自調査（ツールの実装、生成 AI への質問等）の結果を加筆しています。
    - ペイロード（日本語）は、英語のペイロードを基に独自に日本語化しています。
    - すべてのペイロードを検証していないので、期待どおり動作するかはわかりませんし、検証の有無にかかわらず内容は無保証です。
