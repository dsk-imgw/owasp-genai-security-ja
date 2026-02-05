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



## 🟩 AI インフラストラクチャのテスト



## 🟨 AI データのテスト


