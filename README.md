# OWASP GenAI Security (Japanese)

OWASP が発行した生成 AI セキュリティに関するホワイト ペーパー/ガイドを勝手に（＝非公式）日本語にしてみたものです。参考までにどうぞ・・・。それぞれに Markdown ファイルと PDF ファイルがありますが、Markdown では網掛けや斜字等がうまく表現されないので、その辺を気にするのであれば PDF 版をご確認ください。

- [GenAI Red Teaming Guide](https://genai.owasp.org/resource/genai-red-teaming-guide/) ... 生成 AI に対するレッド チーミングに関するガイド v1.0
  - [genai-red-teaming-guide](https://github.com/dsk-imgw/owasp-genai-security-ja/tree/main/genai-red-teaming-guide) ディレクトリ配下
- [Agentic AI – Threats and Mitigations](https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/) ... エージェント型 AI（AI エージェント）の脅威と軽減策に関するガイダンス v1.0
  - [agentic-ai-threat-and-mitigations](https://github.com/dsk-imgw/owasp-genai-security-ja/tree/main/agentic-ai-threat-and-mitigations) ディレクトリ配下
- [A Guide To Preparing and Responding To Deepfake Events](https://genai.owasp.org/resource/guide-for-preparing-and-responding-to-deepfake-events/) ... ディープフェイクへの準備と対応に関するガイド v1.0
  - [a-guide-to-preparing-and-responding-to-deepfake-events](https://github.com/dsk-imgw/owasp-genai-security-ja/tree/main/a-guide-to-preparing-and-responding-to-deepfake-events) ディレクトリ配下
- [AIMA - AI Maturity Assessment](https://github.com/OWASP/www-project-ai-maturity-assessment) ... AI 成熟度モデル評価（2025/7/2 時点で DRAFT 版ベース。）
  - [ai-maturity-assessment](https://github.com/dsk-imgw/owasp-genai-security-ja/tree/main/ai-maturity-assessment) ディレクトリ配下（Excel ファイルは、[OWASP SAMM v2 のツールキットにある評価シート](https://github.com/OWASP/samm/blob/master/Supporting%20Resources/v2.0/toolbox/SAMM_Assessment_Toolbox_v2.0.xlsx)をもとに独自に制作）

## 上記以外で気になっているプロジェクト

- [Artificial Intelligence Vulnerability Scoring System (AIVSS)](https://github.com/OWASP/www-project-artificial-intelligence-vulnerability-scoring-system) ... AI の脆弱性によるリスクを定量化するためのフレームワーク。CVSS の AI 版という感じ。
- [OWASP Artificial Intelligence Security Verification Standard (AISVS)](https://github.com/OWASP/AISVS) ... AI セキュリティの検証基準（検証要件）。ASVS (Application Security Verification Standard) の AI 版という感じ。ASVS と同じく、要件（＝何を検証するか？）のみ記載され、検証方法（＝どうやって検証するか）は記載されていません。
- [OWASP AI Testing Guide](https://github.com/OWASP/www-project-ai-testing-guide/) ... AI セキュリティのテスト方法をまとめたもの。WSTG (Web Security Testing Guide) の AI 版という感じ。なお、AISVS 要件とのリンクがない（AISVS 要件との対応関係が未定義な）ため、リンクさせたい場合はご自身で対応する必要があります。
