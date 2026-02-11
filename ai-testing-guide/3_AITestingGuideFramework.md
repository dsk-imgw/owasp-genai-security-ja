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
	<td><a href="https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-07_Testing_for_Goal_Alignment.md">目標との整合のテスト</a></td>
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

LLM/生成 AIシステム、特にマルチ エージェント アーキテクチャを採用しているシステムにおいて、純粋なブラックボックス テストを実施すると、大きな制限と複雑さが増す可能性があります。

ブラックボックス アプローチを用いた評価活動を計画する際には、以下の**制限事項**を考慮する必要があります。

- LLM モデルは**数値的な重みと数学関数**で構成されており、ソース コードに記述されたワークフローには従いません。従来のアプリケーションでは、ソース コードを解析することで特定の問題の有無を特定できることが多いですが、**生成 AI アプリケーションでは、これは複雑になるか、全く実行不可能になる可能性があります**。
- 多くの LLM モデルは、0 より大きい**温度**値を使用します。温度は、モデルの出力のランダム性を制御するパラメータです。温度が高いほど、より広い範囲のトークンからサンプリングすることでランダム性と「創造性」が高まり、より多様で決定論的ではない出力が生成されます。これにより、**攻撃ベクトルを複数回繰り返す**必要が生じ、結果の**再現が困難**になる可能性があります。温度がゼロの場合でも、浮動小数点演算の非結合性により、評価バッチ サイズ、GPU 数、または GPU バージョンを変更すると、結果が再現不可能になり、大幅に異なる可能性があります。
- **ガードレール**自体は LLM モデルを使用して実装されることが多く、分析がさらに複雑になります。
- **複数のエージェント**で構成される 生成 AI アプリケーションでは、通常、ユーザーの入力は最初のプロンプトに含まれ、最初の LLM エージェントの出力が次の LLM エージェントの入力になります。このプロセスは、生成 AI システムのアーキテクチャとユーザーが提供する具体的な入力に応じて、複数回繰り返されることがあります。このようなアーキテクチャでは、アプリケーションのさまざまなコンポーネントすべてを効果的に検証することは特に複雑であり、**そのような分析に必要な時間とリクエスト数は法外なものになるか、場合によってはまったく実現不可能になる可能性があります**。
- 多くの 生成 AI アプリケーションは、**業界の主要企業が提供する外部モデル**に依存しています。これらのモデルは、通常、**入力と出力の両方で処理されるトークンの数に基づいてコストがかかります**。一部のモデルでは、このコストは相当な額になる可能性があり、**大規模な自動テストを検討する前に**考慮する必要があります。そのため、このようなアプリケーションではトークン消費量を制限するためのしきい値が設定されていることが多く、トークンの無制限な使用は**サービス拒否 (DoS)** または**ウォレット拒否 (DoW)** 状態につながる可能性があります。また、マルチ エージェント システムでは、トークン消費はユーザーの入力とアプリケーションの最終出力だけでなく、エージェント間で交換されるすべての中間プロンプトと出力も含まれることを考慮することが重要です。これにより、全体的なトークン使用量が大幅に増加することがよくあります。

以下の**要件**は、時間とリソースの消費を抑えながらより良い結果をもたらす可能性がありますが、より多くの情報が必要となるため、**よりグレーボックスまたはホワイトボックス的なアプローチが必要になります**。

- **詳細なアプリケーション ログへのアクセス**: 生成 AI アプリケーション、特にマルチ エージェント アーキテクチャを採用したアプリケーションの開発では、エージェント間のインタラクションや、エージェントが受信および生成する入出力を可視化するために、開発者は通常ロギング ツールを使用します。このようなツールを利用できることで、**より標的を絞ったテストが可能になり**、トークン使用量や検証時間といったリソース消費を削減できます。
- プロンプト、アーキテクチャ、ソース コードへのアクセス: テスト中に利用できる情報が多いほど、特定のアプリケーションとそのプロンプトに合わせたテストを実行できる可能性が高まり、**必要なテスト数と時間の両方を削減できます**。生成 AI テストでは、前述の制約（温度、コストなど）があるため、これは**標準的なアプリケーション テストよりも非常に重要です**。
- **サードパーティー サービスの管理コンソールへの読み取りアクセス**: サードパーティーの LLMに基づくアプリケーションの使用に関連する重大なリスク（サービス拒否攻撃やウォレット拒否攻撃など）を評価するには、これらのサービスの設定を分析する必要があります。これらの管理コンソールには、**使用されているモデル、コストとしきい値、ログ、ガードレール設定、ソース コード、実装されたソリューションのアーキテクチャに関する詳細情報**が含まれている場合があります。

## 3.1 AI アプリケーションのテスト

**AI アプリケーションのテスト**のカテゴリは、AI システム、エンド ユーザー、外部データ ソース間のインタラクションに起因して生じるセキュリティ、安全性、および信頼性に関するリスクに対処します。このテスト カテゴリでは、プロンプト インジェクション、機密データの漏洩、安全でない出力や偏った出力など、AI 駆動型インタラクションに特有の脆弱性を発見し軽減することを目的として、ユーザー入力の処理、出力の生成、実行時インタラクションの処理における AI アプリケーションの動作を評価します。

AI アプリケーションはユーザーや外部環境に直接公開されるため、この層でのテストは、不正アクセス、AI 動作の操作、コンプライアンス違反を防ぐために不可欠です。このカテゴリでは、敵対的なプロンプト操作、安全でない出力、エージェントの不正動作、モデルの抽出やエンベディング操作に関連するリスクなど、明確に定義された脅威シナリオに対する包括的な評価が対象となります。

### このテスト カテゴリの範囲

このカテゴリでは、AI アプリケーションの以下の点を評価します。

- **プロンプト操作およびインジェクション攻撃**に対する耐性があるか否か。
	- →  [AITG-APP-01: プロンプト インジェクションのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-01_Testing_for_Prompt_Injection.md)
	- →  [AITG-APP-02: 間接プロンプト インジェクションのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-02_Testing_for_Indirect_Prompt_Injection.md)

- 機密データの漏洩を防ぐための**情報境界**を維持しているか否か。
	- →  [AITG-APP-03: 機密データの漏洩のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-03_Testing_for_Sensitive_Data_Leak.md)
	- →  [AITG-APP-04: 入力の漏洩のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-04_Testing_for_Input_Leakage.md)
	- →  [AITG-APP-07: プロンプトの開示のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-07_Testing_for_Prompt_Disclosure.md)

- **安全で、偏りがなく、適切に調整された出力**を生成しているか否か
	- →  [AITG-APP-05: 安全でない出力のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-05_Testing_for_Unsafe_Outputs.md)
	- →  [AITG-APP-10: 危害を及ぼすコンテンツ バイアスのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-10_Testing_for_Harmful_Content_Bias.md)
	- →  [AITG-APP-11: 幻覚のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-11_Testing_for_Hallucinations.md)
	- →  [AITG-APP-12: 有害な出力のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-12_Testing_for_Toxic_Output.md)

- **エージェント型の動作と運用上の制限**を効果的に管理しているか否か
	- →  [AITG-APP-06: エージェント型動作の制限のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-06_Testing_for_Agentic_Behavior_Limits.md)
	- →  [AITG-APP-13: AI への過度な依存のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-13_Testing_for_Over-Reliance_on_AI.md)

- AI の意思決定に**説明可能性と解釈可能性**を提供しているか否か
	- →  [AITG-APP-14: 説明可能性および解釈可能性のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-14_Testing_for_Explainability_and_Interpretability.md)

- **エンベディング ベースの攻撃やモデル抽出の試み**から保護されているか否か
	- →  [AITG-APP-08: エンベディングの操作のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-08_Testing_for_Embedding_Manipulation.md)
	- →  [AITG-APP-09: モデル抽出のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-APP-09_Testing_for_Model_Extraction.md)

AI アプリケーション テストのカテゴリ内の各テストは、アプリケーション レベルのリスクに体系的に対処し、実環境における堅牢な運用を確保し、組織が倫理基準や規制を遵守できるようにすることで、AI システムの包括的なセキュリティ態勢の構築に貢献します。

## 3.2 AI モデルのテスト

**AI モデルのテスト**のカテゴリは、デプロイメントのコンテキストに関わらず、AI モデル自体の脆弱性と堅牢性に焦点を当てています。このカテゴリは、AI モデルの本質的な特性と動作に特に焦点を当て、敵対的な状況下でも確実に動作し、機密情報を漏洩せず、意図された目標に沿った動作を維持することを保証します。

モデル レベルでのテストは、回避攻撃、データ汚染、プライバシー漏洩、不整合問題といった根本的な弱点を検出するのに役立ちます。これらの弱点は、モデルのすべてのデプロイメントに波及する可能性があります。包括的なモデルのテストは、AI システムの完全性、セキュリティ、信頼性を維持するために不可欠です。

### このテスト カテゴリの範囲

このカテゴリでは、AI モデルの以下の点を評価します。

- **敵対的な回避攻撃**に対して堅牢かつ回復力があるか否か
	- →  [AITG-MOD-01: 回避攻撃のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-01_Testing_for_Evasion_Attacks.md)

- **実行時のモデル汚染**から効果的に保護されているか否か
	- →  [AITG-MOD-02: 実行時のモデル汚染のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-02_Testing_for_Runtime_Model_Poisoning.md)

- **学習時の汚染攻撃**に耐性があるか否か
	- →  [AITG-MOD-03: 汚染済み学習セットのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-03_Testing_for_Poisoned_Training_Sets.md)

- 推論攻撃および反転攻撃から**データ プライバシー**を保護しているか否か
	- →  [AITG-MOD-04: メンバーシップ推論のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-04_Testing_for_Membership_Inference.md)
	- →  [AITG-MOD-05: 反転攻撃のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-05_Testing_for_Inversion_Attacks.md)

- **新規データまたは敵対的なデータが提示された場合でも堅牢性**を維持できるか否か
	- → [AITG-MOD-06: 新規データへの堅牢性のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-06_Testing_for_Robustness_to_New_Data.md)

- **事前に定義された目標および制約と**一貫して**整合**しているか
	- →  [AITG-MOD-07: 目標との整合のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-MOD-07_Testing_for_Goal_Alignment.md)

AI モデルのテスト カテゴリ内の各テストは、AI モデルの基本的な回復力、信頼性、安全性を確保し、すべてのデプロイメントとアプリケーションにわたるシステム リスクを軽減するのに役立ちます。

## 3.3 AI インフラストラクチャのテスト

**AI インフラストラクチャのテスト**は、AI モデルのデプロイメントと運用を支える技術インフラストラクチャとコンポーネントにおける脆弱性とリスクを対象としています。この部門では、モデルのサプライチェーン、リソース管理、境界制御、プラグイン、微調整環境、そしてモデルへの不正アクセスや悪用を防ぐ仕組みなど、インフラストラクチャレベルのセキュリティを特に検証します。

インフラストラクチャ レベルの脆弱性は、不正アクセス、リソース枯渇、モデルや関連コンポーネントの改ざんといった重大な問題につながる可能性があります。包括的なインフラストラクチャ テストを実施することで、これらのシステムが安全に構成され、悪用や悪用に対する耐性を備え、サポートする AI システムを保護できることが保証されます。

### このテスト カテゴリの範囲

このカテゴリでは、AI インフラストラクチャの以下の点を評価します。

- **サプライチェーンの改ざんと不正な改変**を防止しているか否か
	- →  [AITG-INF-01: サプライチェーン改ざんのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-01_Testing_for_Supply_Chain_Tampering.md)

- **リソース枯渇とサービス拒否状態**に対する耐性があるか否か
	- →  [AITG-INF-02: リソース枯渇のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-02_Testing_for_Resource_Exhaustion.md)

- プラグイン ベースのインタラクションに対してセキュアな境界とアクセス制御を維持しているか否か
	- →  [AITG-INF-03: プラグインの境界違反のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-03_Testing_for_Plugin_Boundary_Violations.md)

- **モデルの機能と関数の悪用**に対する厳格な制御を実施しているか否か
	- →  [AITG-INF-04: 機能の悪用のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-04_Testing_for_Capability_Misuse.md)

- **モデルの微調整**に使用される環境を**汚染と破損から**保護しているか否か
	- →  [AITG-INF-05: 微調整時の汚染のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-05_Testing_for_Fine-tuning_Poisoning.md)

- **開発フェーズにおけるモデルの盗難または漏洩**を防止しているか否か
	- →  [AITG-INF-06: 開発時のモデル盗難のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-INF-06_Testing_for_Dev-Time_Model_Theft.md)

AI インフラストラクチャのテストのカテゴリ内の各テストは、AI システムに必要な基本的なセキュリティ態勢に貢献し、モデルのライフサイクル全体にわたって脅威を防止および軽減できる、信頼性が高く、安全で、堅牢なインフラストラクチャを保証します。

## 3.4 AI データのテスト

AI データのテストのカテゴリは、学習データセット、推論入力、実行時インタラクションなど、AI ライフサイクル全体を通じて利用されるデータの検証と保護に重点を置いています。このカテゴリでは、データ品質の検証、堅牢なプライバシー保護の確保、データセットのカバレッジ評価、有害または不適切なコンテンツによる AI システムへの悪影響の防止を重視しています。

データ関連の脆弱性は、プライバシー侵害やデータ流出から、バイアスや安全でないモデルの動作まで、幅広い影響を及ぼす可能性があります。包括的な AI データのテストは、データセットの多様性、コンプライアンス、セキュリティ、適切性を体系的に評価することでこれらのリスクに対処し、AI アプリケーションの倫理的、堅牢、かつ安全な運用を保証します。

### このテスト カテゴリの範囲

このカテゴリでは、AI データの以下の点を評価します。

- **機密性の高い学習データの意図しない公開や漏洩**を防止しているか否か
	- → [AITG-DAT-01: 学習データの意図せぬ公開のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-01_Testing_for_Training_Data_Exposure.md)

- **機密情報や個人情報の実行時の持ち出し**に対してセキュリティが確保されているか否か
	- →  [AITG-DAT-02: 実行時の持ち出しのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-02_Testing_for_Runtime_Exfiltration.md)

- バイアスやパフォーマンス ギャップを回避するために、**十分な多様性、表現、包括的なカバレッジ**を提供しているか否か
	- →  [AITG-DAT-03: データセットの多様性と網羅性のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-03_Testing_for_Dataset_Diversity_and_Coverage.md)

- 危害を及ぼす、有害な、またはバイアスのあるコンテンツが含まれていないか否か
	- →  [AITG-DAT-04: データ内の危害を及ぼすコンテンツのテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-04_Testing_for_Harmful_Content_in_Data.md)

- 規制やプライバシーのベスト プラクティスで義務付けられている**データ最小化の原則と同意要件**と整合しているか否か
	- →  [AITG-DAT-05: データの最小化および同意のテスト](https://github.com/OWASP/www-project-ai-testing-guide/blob/main/Document/content/tests/AITG-DAT-05_Testing_for_Data_Minimization_and_Consent.md)

AI データのテストのカテゴリ内の各テストでは、AI モデルを強化するデータセットが重要な品質、倫理、セキュリティ、コンプライアンスの標準を満たしていることを確認し、最終的にはより安全で責任ある AI システムの実現に貢献します。
