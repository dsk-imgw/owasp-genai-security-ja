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


