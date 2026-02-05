# 3. AI Testing ガイド フレームワーク

第 2 章で実施した脅威モデリングに基づき、AI アーキテクチャの脅威を具体的なテスト ケースにマッピングする構造化フレームワークを定義できるようになりました。このプロジェクトは、従来のサイバー セキュリティ、MLOps テスト、そして責任ある AI 評価を統一された構造の下で橋渡しすることを目的としています。

各テスト ケースは、以下の 4 つの柱のいずれかに分類されます。

- 🟦 AI アプリケーションのテスト
- 🟪 AI モデルのテスト
- 🟩 AI インフラストラクチャのテスト
- 🟨 AI データのテスト

分析を開始する前に、この種類のテストの限界を考慮し、ブラックボックス アプローチからグレーボックスまたはホワイトボックス アプローチへの移行の可能性を検討することが重要です。これには追加情報が必要です。限界と要件については、次の段落で説明します。

## 🟦 AI アプリケーションのテスト

<table width="100%">
<tr>
	<th width="15%">テスト ID</th>
	<th width="45%">テスト名＆リンク</th>
	<th width="25%">脅威のソース</th>
	<th width="15%">ドメイン</th>
</tr>
<tr>
	<td>AITG-APP-01</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-01_Testing_for_Prompt_Injection.md">プロンプト インジェクションのテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-APP-02</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-02_Testing_for_Indirect_Prompt_Injection.md">間接プロンプト インジェクションのテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-APP-03</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-03_Testing_for_Sensitive_Data_Leak.md">機密データの漏洩のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ、プライバシー</td>
</tr>
<tr>
	<td>AITG-APP-04</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-04_Testing_for_Input_Leakage.md">入力の漏洩のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ、プライバシー</td>
</tr>
<tr>
	<td>AITG-APP-05</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-05_Testing_for_Unsafe_Outputs.md">安全でない出力のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ、RAI</td>
</tr>
<tr>
	<td>AITG-APP-06</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-06_Testing_for_Agentic_Behavior_Limits.md">エージェント型動作の制限のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ、RAI</td>
</tr>
<tr>
	<td>AITG-APP-07</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-07_Testing_for_Prompt_Disclosure.md">プロンプトの開示のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ、プライバシー</td>
</tr>
<tr>
	<td>AITG-APP-08</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-08_Testing_for_Embedding_Manipulation.md">エンベディングの操作のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-APP-09</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-09_Testing_for_Model_Extraction.md">モデル抽出のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-APP-10</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-10_Testing_for_Harmful_Content_Bias.md">危害を及ぼすコンテンツ バイアスのテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-APP-11</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-11_Testing_for_Hallucinations.md">幻覚のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-APP-12</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-12_Testing_for_Toxic_Output.md">有害な出力のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-APP-13</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-13_Testing_for_Over-Reliance_on_AI.md">AI への過度な依存のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-APP-14</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-14_Testing_for_Explainability_and_Interpretability.md">説明可能性および解釈可能性のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
</table>

## 🟪 AI モデルのテスト

<table width="100%">
<tr>
	<th width="15%">テスト ID</th>
	<th width="45%">テスト名＆リンク</th>
	<th width="25%">脅威のソース</th>
	<th width="15%">ドメイン</th>
</tr>
<tr>
	<td>AITG-MOD-01</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-01_Testing_for_Evasion_Attacks.md">回避攻撃のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-MOD-02</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-02_Testing_for_Runtime_Model_Poisoning.md">実行時のモデル汚染のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-MOD-03</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-03_Testing_for_Poisoned_Training_Sets.md">汚染済み学習データセットのテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-MOD-04</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-04_Testing_for_Membership_Inference.md">メンバーシップ推論のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>プライバシー</td>
</tr>
<tr>
	<td>AITG-MOD-05</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-05_Testing_for_Inversion_Attacks.md">反転攻撃のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>プライバシー</td>
</tr>
<tr>
	<td>AITG-MOD-06</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-06_Testing_for_Robustness_to_New_Data.md">新規データへの堅牢性のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-MOD-07</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-07_Testing_for_Goal_Alignment.md">ゴールとの整合のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
</table>

## 🟩 AI インフラストラクチャのテスト

<table width="100%">
<tr>
	<th width="15%">テスト ID</th>
	<th width="45%">テスト名＆リンク</th>
	<th width="25%">脅威のソース</th>
	<th width="15%">ドメイン</th>
</tr>
<tr>
	<td>AITG-INF-01</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-01_Testing_for_Supply_Chain_Tampering.md">サプライチェーン改ざんのテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-INF-02</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-02_Testing_for_Resource_Exhaustion.md">リソース枯渇のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-INF-03</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-03_Testing_for_Plugin_Boundary_Violations.md">プラグインの境界違反のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-INF-04</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-04_Testing_for_Capability_Misuse.md">機能の悪用のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-INF-05</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-05_Testing_for_Fine-tuning_Poisoning.md">微調整時の汚染のテスト</a></td>
	<td>OWASP Top 10 LLM 2025</td>
	<td>セキュリティ</td>
</tr>
<tr>
	<td>AITG-INF-06</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-06_Testing_for_Dev-Time_Model_Theft.md">開発時のモデル盗難のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>セキュリティ、プライバシー</td>
</tr>
</table>

## 🟨 AI データのテスト


<table width="100%">
<tr>
	<th width="15%">テスト ID</th>
	<th width="45%">テスト名＆リンク</th>
	<th width="25%">脅威のソース</th>
	<th width="15%">ドメイン</th>
</tr>
<tr>
	<td>AITG-DAT-01</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-01_Testing_for_Training_Data_Exposure.md">学習データの意図せぬ公開のテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>プライバシー</td>
</tr>
<tr>
	<td>AITG-DAT-02</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-02_Testing_for_Runtime_Exfiltration.md">実行時の持ち出しのテスト</a></td>
	<td>OWASP AI Exchange</td>
	<td>セキュリティ、プライバシー</td>
</tr>
<tr>
	<td>AITG-DAT-03</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-03_Testing_for_Dataset_Diversity_and_Coverage.md">データセットの多様性および網羅性のテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-DAT-04</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-04_Testing_for_Harmful_Content_in_Data.md">データ内の危害を及ぼすコンテンツのテスト</a></td>
	<td>Responsible AI</td>
	<td>RAI</td>
</tr>
<tr>
	<td>AITG-DAT-05</td>
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-05_Testing_for_Data_Minimization_and_Consent.md">データの最小化および同意のテスト</a></td>
	<td>Responsible AI</td>
	<td>プライバシー、RAI</td>
</tr>
</table>

## テストの制限事項と要件

