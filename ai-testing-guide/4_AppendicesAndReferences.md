# 4. 付録と参考情報

## はじめに

この章では、OWASP AI Testing Guide の本文を補完するすべてのサポート資料を提供します。付録では、ガイドで提案されている方法論を補強する、構造化されたフレームワーク、脅威モデル、リスク ライフサイクル、およびドメイン固有のガイダンスを提供します。

これらのリソースは、主に以下の 3 つの目的に役立ちます。

1. 本書の前半で紹介した概念を**深化させます**。
2. モデル、マッピング、および方法論を通じて AI テストを**運用可能にします**。
3. 業界標準、セキュリティ分類、および学術文献に基づいてガイドを**構築します**。

本章の最後には、ガイド全体で使用されているすべての情報源を網羅した**参考情報**セクションがあります。

### 4.1 付録 A: SAIF (Secure AI Framework) 採用の根拠

付録 Aでは、信頼できる AI 開発とテストの基盤モデルとして SAIF (Secure AI Framework) を採用した根拠について説明します。

SAIF は以下の特長を備えています。

- データ、モデル、アプリケーション、インフラストラクチャ層を網羅する包括的な構造
- AI システムに合わせたセキュア・バイ・デザインの視点
- 最新のリスク分類法とガバナンス フレームワークとの整合性
- 脅威、リスク、アーキテクチャに関する付録との概念的な連続性

この付録では、AI が従来のソフトウェア テスト パラダイムを超えたフレームワークを必要とする理由を説明します。

### 4.2 付録 B: 分散化 (Distributed)、不変 (Immutable)、一時的 (Ephemeral)（DIE）による脅威の特定

この付録では、クラウド ネイティブおよび最新の AI 環境における脅威を特定するためのレンズとして、DIE モデル（分散化、不変、一時的）を紹介します。

AI システムには、多くの場合、次のような要素が含まれます。

- 分散コンピューティング クラスタ
- 不変のアーティファクト（コンテナ、モデル バイナリなど）、
- 一時的なジョブ（学習パイプライン、マイクロ サービスなど）

これらの特性により、固有の攻撃対象領域が生まれます。DIE フレームワークは、サプライチェーン インジェクション、改ざんされたアーティファクト、ワークフロー操作、クラウド環境の悪用といった脅威をテスターが認識するのに役立ちます。

### 4.3 付録 C: セキュアな AI システムのリスク ライフサイクル

付録 Cでは、AI システムの動的かつ進化する性質を反映した、AI 固有のリスク ライフサイクルについて説明します。

ライフサイクルには、以下の内容が含まれます。

- リスクの特定
- 発生可能性と影響の評価
- 軽減戦略の設計
- ドリフトや敵対者による操作の監視
- 残存リスクのレビューと管理策の更新

データ ドリフト、モデル ドリフト、フィードバック ループ リスクなど、AI システムに固有の現象には特に注意を払います。

### 4.4 付録 D: AI アーキテクチャ コンポーネントへの脅威一覧

この付録では、AI アーキテクチャ コンポーネント全体にわたる脅威の構造化されたマッピングを提供します。これには、以下が含まれます。

- データ層
- モデル層
- アプリケーション/API 層
- インフラストラクチャ、およびデプロイメント環境

各コンポーネントについて、付録では以下の詳細を説明します。

- 主要な脅威ベクトル
- 一般的な脆弱性
- 層間の伝播効果

この一覧は、本ガイドの前半で定義したテスト手順の基礎となります。

### 4.5 付録 E: AI システムの脆弱性（CVE および CWE）に対する AI 脅威のマッピング

付録 Eでは、AI 固有の脅威を、以下の既存の脆弱性分類と関連付けています。

- CWE（共通脆弱性列挙）
- CVE（共通脆弱性識別子）
- 関連する MITRE 分類

このマッピングは、モデル抽出、プロンプト インジェクション、学習データ漏洩といった脅威が、従来のソフトウェア脆弱性クラスとどのように関連しているかを示しています。目標は、AI セキュリティ テストを既存のエンタープライズ脆弱性管理ワークフローに統合することです。

### 4.6 参考情報

最後のセクションでは、このガイド全体で引用されているすべての情報源（標準規格、学術研究、業界論文、オープン ソース プロジェクトなど）をまとめています。これらの参考情報は、OWASP AI Testing Guide で概説されているフレームワーク、方法論、推奨事項を裏付ける基礎資料を提供します。

-------------------------------------------------------------------

## 4.1 付録 A: AI 脅威モデリングのアーキテクチャ適用範囲として SAIF を選択した理由

AI 脅威モデリングのアーキテクチャ適用範囲として Google の SAIF を採用した理由は、システムをデータ、モデル、アプリケーション、インフラストラクチャの各層に明確に分解し、構造化されたテストとセキュリティ管理策の整合を可能にするためです。

OWASP AI セキュリティ マトリックスは、脅威に焦点を当て、潜在的な攻撃対象を中心に構成されていますが、SAIF は防御とセキュア設計に重点を置いています。両フレームワークは高度に補完的です。SAIF はセキュリティ保護の対象を定義するのに役立ち、OWASP はセキュリティ保護の対象を定義するのに役立ちます。どちらも強固な基盤として機能し、実際には、両方を整合させることで脅威の網羅性とアーキテクチャの追跡可能性が強化されます。

ここでは、OWASP AI セキュリティ マトリックスで定義されている AI アーキテクチャ コンポーネントと、Google の SAIF (Secure AI Framework) で定義されている AI アーキテクチャ コンポーネントを比較します。これにより、各フレームワークの共通の重点分野と固有の要素をマッピングすることで、脅威モデリングとセキュリティ テストの取り組みを整合させることができます。

<div align="center">
コンポーネントにおける OWASP AI セキュリティ マトリックスと Google SAIF の比較
	
<table>
<tr>
	<th width="20%">コンポーネント カテゴリ</th>	
	<th width="20%">OWASP AI セキュリティ マトリックス</th>	
	<th width="20%">Google SAIF アーキテクチャ</th>	
	<th width="40%">コメント</th>	
</tr>
<tr>
	<td>データ</td>
	<td>学習データ、入力データ、出力データ</td>
	<td>データ（学習、推論、変換、取り込みに渡ります	）</td>
	<td>どちらも学習と入力データの完全性を含みますが、SAIF はデータのライフサイクルをより包括的に扱います。</td>
</tr>
<tr>
	<td>モデル</td>
	<td>モデル アーキテクチャ、モデル パラメータ、モデル アーティファクト、モデル出力</td>
	<td>モデル（入力の処理、利用、出力の処理）</td>
	<td>OWASP はモデルをアーティファクトとアーキテクチャに分割し、SAIF は実行時とガードレールを強調します</td>
</tr>
<tr>
	<td>アプリケーション</td>
	<td>プロンプト インターフェース、API、プラグイン、出力チャネル</td>
	<td>アプリケーション、エージェント/プラグイン、ユーザー入出力</td>
	<td>強力な整合性: OWASP「プロンプト インターフェース」= SAIF「ユーザー入力」; プラグイン/コンポーネントも同じく整合</td>
</tr>
<tr>
	<td>インフラストラクチャ</td>
	<td>モデルのデプロイメント環境、CI/CD パイプライン、クラウド プラットフォーム/ホスティング</td>
	<td>インフラストラクチャ、モデル サービング、モデル ストレージ、モデル評価、学習インフラ</td>
	<td>OWASP と SAIFは、どちらもデプロイメント環境と実行時環境に重点を置いていますが、SAIF はよりきめ細かです。</td>
</tr>
<tr>
	<td>セキュリティ ガバナンス</td>
	<td>監視、ログ記録、アクセス制御</td>
	<td>ログ記録＆監査、アクセス制御、アイデンティティと認証</td>
	<td>どちらのフレームワークにも、テスト、追跡可能性、制御に不可欠なガバナンス コンポーネントが含まれています。</td>
</tr>
<tr>
	<td>外部依存関係</td>
	<td>サードパーティーのデータ フィード、事前学習済みモデル、API/LLM</td>
	<td>外部ソース、プラグイン統合</td>
	<td>SAIF は信頼境界を明示的に指定し、OWASP はサードパーティー モデルのリスクに対処します。</td>
</tr>

</table>
</div>

### 4.2 付録 B: 分散化 (Distributed)、不変 (Immutable)、一時的 (Ephemeral)（DIE）による脅威の特定

AI モデルは大規模に運用され、高度に動的なデータフローに依存し、しばしば不透明な「ブラックボックス」として機能するため、予期せぬ障害モードや攻撃対象領域が生じる可能性があります。この問題に対処するため、DIE トライアド（分散化、不変、一時的）は、補完的で回復力に重点を置いたフレームワークを提供します。Sounil Yu [20] によって最初に提唱された DIE モデルは、従来のデータ保護からシステムの生存性、適応性、そしてアーキテクチャの堅牢性へと焦点を移しています。モデルのドリフト、敵対的な入力、依存関係の連鎖が常に懸念される AI の文脈において、DIE 原則を適用することで、AI システムがセキュアであるだけでなく、設計上回復力を備え、中断や劣化に耐えられることを保証できます。

CIA（機密性、完全性、可用性）は、データとシステムを不正アクセスや中断から保護することに重点を置いていますが、DIE は、以下の点を重視する設計原則を通じて、攻撃対象の価値と寿命を低減することに重点を移しています。

- **分散化** – **システムは単一障害点に依存してはなりません**。ワークロード、データ、サービスは、回復力、スケーラビリティ、フォールト トレランスを確保するために、複数のノードに分散されます。
- **不変** – **コンポーネント、特にコードとデータは、デプロイ後に変更されてはなりません**。これにより、改ざんが制限され、ロールバックが簡素化され、監査可能性と予測可能性が確保されます。
- **一時的** – **システムは設計上、短命である必要があります**。コンテナ、関数、セッション、データはすぐに期限切れになるよう設計することで、攻撃の機会を減らし、侵害が発生した場合のリスクを最小限に抑えます。

CIA がデータ保護を目的とするのに対し、DIE は、たとえ侵害を受けたとしても本質的に侵害に耐性のあるシステムを設計することを目的としています。CIA と DIE を組み合わせることで、補完的なセキュリティとレジリエンス戦略を実現できます。これは、AI、サーバーレス、マイクロ サービス環境において特に重要です。CIA は不正アクセスの防止や稼働時間の確保といった*セキュリティ目標*の定義に優れていますが、DIE は*アーキテクチャのレジリエンスと信頼性*に重点を置いており、特にクラウド ネイティブ AI システム、LLM エージェントおよびプラグイン アーキテクチャ、連合学習、エッジ AI において重要です。

現代の AI システムの多くの障害（例: 共有 GPU 内のデータ残存、ホット リロードされた LLM エージェント、分散パイプラインのドリフト）は、CIA だけでなく DIE 原則にも違反しています。

以下は、SAIF (Secure AI Framework) アーキテクチャに整合した AI システムにおいて、DIE（分散化、不変、一時的）脅威が CIA（機密性、完全性、可用性）モデルとどのように異なり、どのように補完するかを体系的に説明したものです。


<div align="center">
SAIF アーキテクチャに整合した AI システムにおける DIE と CIA の比較
	
<table>
<tr>
	<th width="20%">SAIF 層</th>	
	<th width="20%">DIE 要素</th>	
	<th width="30%">DIE 脅威の例</th>	
	<th width="40%">CIA で網羅されない理由</th>	
</tr>
<tr>
	<td>インフラストラクチャ</td>
	<td>Ephemeral（一時的）</td>
	<td>サーバーレス推論機能におけるデータの残留</td>
	<td>CIA は静的なデータ保護を想定していますが、環境が本当に短命であるかどうかは評価しません。</td>
</tr>
<tr>
	<td>インフラストラクチャ</td>
	<td>Immutable（不変）</td>
	<td>CI/CD パイプラインにおけるモデルの不適切な不変性</td>
	<td>CIA は不正な変更を網羅しますが、再現性とロールバックの不変性は保証しません。</td>
</tr>
<tr>
	<td>データ</td>
	<td>Distributed（分散化）</td>
	<td>連合学習におけるデータの出所の喪失</td>
	<td>CIA は移動中および保存中のデータを保護しますが、分散環境での一貫性や系統は保護しません。</td>
</tr>
<tr>
	<td>モデル</td>
	<td>Immutable（不変）</td>
	<td>自己修正推論ロジック</td>
	<td>CIA は不正な更新をフラグ付けすることはできますが、動的な内部ロジックの変更（プロンプトの調整など）をフラグ付けすることはできません。</td>
</tr>
<tr>
	<td>アプリケーション</td>
	<td>Ephemeral（一時的）</td>
	<td>チャットボットや RAG システムにおける永続的キャッシュ</td>
	<td>CIA はデータの意図せぬ公開に対処しますが、自動失効やゼロ トレースの設計の要件には対処しません。</td>
</tr>
<tr>
	<td>インフラストラクチャ</td>
	<td>Distributed（分散化）</td>
	<td>マルチ クラウド デプロイメントにまたがる一貫性のないアクセス ポリシー</td>
	<td>CIA はポリシーの存在をチェックしますが、分散システム間での同期や適用はチェックしません。</td>
</tr>
</table>
</div>

以下は、SAIF コンポーネント #1 ～ #18 の DIE 脅威マッピングです。

<div align="center">
アプリケーション層 - DIE 脅威マッピング 

<table>
<tr>
	<th width="30%">SAIF コンポーネント</th>	
	<th width="70%">DIE 脅威</th>	
</tr>
<tr>
	<td>#1 ユーザー</td>
	<td><ul><li>分散化: 複数のアクセス ポイントにまたがるユーザーの偽装<li>不変: 操作を許可するセキュアでないセッション ストレージ<li>一時的: 永続的なセッション トークンまたは有効期限のない認証</ul></td>
</tr>
<tr>
	<td>#2 ユーザー入出力</td>
	<td><ul><li>分散化: UI/API の複数のポイントでの傍受<li>不変: 状態の破損につながる入力の未検証<li>一時的: 古いまたはリプレイされた出力につながるキャッシュ済み応答</ul></td>
</tr>
<tr>
	<td>#3 アプリケーション</td>
	<td><ul><li>分散化: アプリ クラスター内での水平展開<li>不変: 設定の改ざんや実行時ロジックの改ざん<li>一時的: メモリ攻撃に対して脆弱な長期プロセス</ul></td>
</tr>
<tr>
	<td>#4 エージェント/プラグイン</td>
	<td><ul><li>分散化: 連鎖的なプラグインの悪用<li>不変: プラグインのペイロードの改変<li>一時的: 永続的なプラグインの状態によるデータ漏洩</ul></td>
</tr>
<tr>
	<td>#5 外部ソース</td>
	<td><ul><li>分散化: ソースまたは転送中におけるフィードの操作<li>不変: 取り込まれたデータの完全性検証の欠如<li>一時的: 長期間存続する静的な外部データセットへの依存</ul></td>
</tr>
</table>
</div>

<br>

<div align="center">
モデル層 - DIE 脅威マッピング 

<table>
<tr>
	<th width="30%">SAIF コンポーネント</th>	
	<th width="70%">DIE 脅威</th>	
</tr>
<tr>
	<td>#6 入力の処理</td>
	<td><ul><li>分散化: エンド ポイントをまたがる入力データの不正使用<li>不変: 無害化層の迂回<li>一時的: 悪意のあるデータの遅延再処理</ul></td>
</tr>
<tr>
	<td>#7 出力の処理</td>
	<td><ul><li>分散化: 複数のチャネルを介した出力の漏洩<li>不変: モデル応答の偽装または改ざん<li>一時的: 安全でない推論結果の保持</ul></td>
</tr>
<tr>
	<td>#8 モデルの利用</td>
	<td><ul><li>分散化: 反復的または組織的な推論の不正使用<li>不変: 推論経路を変更する悪意のあるプロンプト<li>一時的: 結果のキャッシュによる古い出力の公開</ul></td>
</tr>
</table>
</div>

<div align="center">
インフラストラクチャ層 - DIE 脅威マッピング 

<table>
<tr>
	<th width="30%">SAIF コンポーネント</th>	
	<th width="70%">DIE 脅威</th>	
</tr>
<tr>
	<td>#9 モデル ストレージ インフラストラクチャ</td>
	<td><ul><li>分散化: 盗難モデルの複製<li>不変: ハッシュの不一致の未検出<li>一時的: 使用後に残る一時アーティファクト</ul></td>
</tr>
<tr>
	<td>#10 モデル サービング インフラストラクチャ</td>
	<td><ul><li>分散化: ノードをまたがるスケーラブルな攻撃対象領域<li>不変: コンテナ イメージの破損<li>一時的: 不正使用に脆弱な永続化ソケット</ul></td>
</tr>
<tr>
	<td>#11 モデルの評価</td>
	<td><ul><li>分散化: 評価をまたがる結果の漏洩<li>不変: 偽の指標の長期保存<li>一時的: 本番環境で再利用されるテスト アーティファクト</ul></td>
</tr>
<tr>
	<td>#12 モデルの学習＆調整</td>
	<td><ul><li>分散化: 連合汚染攻撃<li>不変: チェックポイントの侵害<li>一時的: 古い学習データの保持</ul></td>
</tr>
<tr>
	<td>#13 モデル フレームワーク＆コード</td>
	<td><ul><li>分散化: ビルドをまたがる利用ライブラリの感染<li>不変: フレームワークへのコード インジェクション<li>一時的: 悪用可能なデバッグ ファイルの未除去</ul></td>
</tr>
<tr>
	<td>#14 データ ストレージ インフラストラクチャ</td>
	<td><ul><li>分散化: 同期済みシステム経由のデータ持ち出し<li>不変: 古くなった破損したバックアップ<li>一時的: 無防備な状態のままの一時ストア</ul></td>
</tr>
</table>
</div>

<div align="center">
データ層 - DIE 脅威マッピング 

<table>
<tr>
	<th width="30%">SAIF コンポーネント</th>	
	<th width="70%">DIE 脅威</th>	
</tr>
<tr>
	<td>#15 学習データ</td>
	<td><ul><li>分散化: データセットをまたがる汚染<li>不変: 不良データの 1 つのコピー内のみでの修正<li>一時的: 機密データの未変更</ul></td>
</tr>
<tr>
	<td>#16 データのフィルタリング＆処理</td>
	<td><ul><li>分散化: エッジ ノードの不正使用によるフィルター回避<li>不変: 不正な変換の未検出<li>一時的: 処理データの未除去</ul></td>
</tr>
<tr>
	<td>#17 内部データ ソース</td>
	<td><ul><li>分散化: 内部システムを通じた侵害<li>不変: 参照レコードの破損<li>一時的: 過剰なクエリ ログまたはクエリの保持</ul></td>
</tr>
<tr>
	<td>#18 外部データ ソース</td>
	<td><ul><li>分散化: 公開 API の不正使用<li>不変: 取り込み時の完全性の未チェック<li>一時的: ソース コンテンツが安全でない方法での再利用</ul></td>
</tr>
</table>
</div>


## 4.3 付録 C: セキュアな AI システムのリスク ライフサイクル マッピング（SAIF フレームワークに基づく）

以下の表は、Secure AI Framework (SAIF) によって特定された主要な AI リスクが、AI システムのライフ サイクル全体にわたってどのように現れるかを構造的に示しています。各リスクについて、以下の点に重点を置きます。

1. **リスクの発生場所** – 根本原因が発生するシステムのレイヤーまたはコンポーネント（例: セキュアでないデータ取り込み、不適切なモデル学習制御）。
2. **リスクが露呈する場所** – リスクの影響が観測される可能性のある段階またはコンポーネント（例: モデル推論中またはアプリケーション使用中）。
3. **リスクが管理される場所** – リスクの発生可能性または影響を低減するために軽減策を適用できるシステムの部分。
4. **リスクの管理方法** – 具体的な技術的または手順的な対策（例: 入力検証、アクセス制御、CI/CD 検証）。

### 重要な洞察

1. データとインフラストラクチャに起因するリスクは基盤であり、データ汚染、不正な学習データ、モデル ソースの改ざんといったリスクは、データ層とインフラストラクチャ層を通じて発生し、伝播します。これは、パイプラインの初期段階におけるセキュリティ ギャップが下流のコンポーネントに悪影響を及ぼす可能性があることを反映しています。これらのリスクは、以下の点の必要性を浮き彫りにしています。
	- i. データの検証と出所の追跡
	- ii. セキュアなストレージとアクセス制御
	- ii. CI/CD およびアーティファクトの厳格な完全性検証
2. モデル リスクには静的な管理策と実行時の管理策の両方が必要です。モデル回避、モデル リバース エンジニアリング、機密データ漏洩といった脅威は、モデルの動作がデプロイ後に操作または照会される可能性があることを示唆しています。これらには二重の防御層が必要です。
	-  i. 敵対的学習や差分プライバシーなどのデプロイメント前の管理策
	- ii. クエリ監視、出力フィルタリング、行動分析などのデプロイメント後の管理策
3. アプリケーション層は高頻度の攻撃ベクトルをホストします。プロンプト インジェクション、ML サービス拒否、セキュアでない統合コンポーネントなどのリスクにより、アプリケーション層は、特にユーザー向けの LLM インターフェースやエージェント ベースのアーキテクチャにおいて、頻繁に侵害の危険にさらされます。推奨される軽減策は、以下の点に重点を置いています。
	- i. 入力の無害化と検証
	- ii. リクエストのスロットリングと異常検出
	- iii. 信頼境界とプラグインのガバナンス
4. 管理策の実装には多層的な適用が必要です。 多くのリスクは、複数のSAIF 層にまたがって制御されます。例えば、以下のような例があります。
	- 推論された機密データには、モデル層（プライバシー保護技術）とデータ層（アクセス制限）の両方の管理策が必要です。
	- モデルの持ち出しはインフラストラクチャ（公開 API 経由など）に影響を及ぼすだけでなく、エンベディングや重みへのアクセス時にモデル層にも影響を及ぼします。これは、複雑な脅威ベクトルに対して単一点の管理策では不十分な、**多層防御**の必要性を浮き彫りにしています。
5. 実行時のガバナンスと可観測性が重要です。 多くのリスク（例: モデルのリバース エンジニアリング、不正なアクション、ML サービス拒否）において、実行時の可観測性とポリシー適用機構（レート制限、サンドボックス、出力モデレーションなど）は、動的な環境における新たな AI 脅威の軽減に不可欠です。


（表）

## 4.4 付録 D: 露出コンポーネントに関する SAIF リスクの OWASP LLM Top 10および AI Exchange 脅威への マッピング

このセクションでは、OWASP LLM Top 10 および OWASP AI Exchange から主要な AI 関連セキュリティ脅威を列挙し、それらの SAIF リスクへのマッピングを示します。各エントリには、簡潔な脅威の説明と、マッピングされた SAIF コンポーネントに基づく仮想的な脅威シナリオが含まれています。これらのシナリオは、有意義なテスト ケースを導き出し、軽減策の有効性を検証するのに役立ちます。

### T01-DPIJ - 直接プロンプト インジェクション

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-IPIJ - 間接プロンプト インジェクション

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-AIE - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-RMP - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-DMP - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-DPFT - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-SCMP - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-SID - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-MIMI - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-RMP - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-TDL - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-MTU - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-MTR - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-MTD - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-DoSM - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-LSID - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-IOH - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-EA - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-SPL - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-VEW - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

### T01-MIS - xxx

- **OWASP LLM**: 
- **SAIF リスク**: 
- **解説**: 
- **脅威シナリオ**: 

以下の表は、OWASP Top 10 for LLMs (2025) を含む OWASP AI 関連の脅威と、リスクにさらしている Secure AI Framework (SAIF) コンポーネントとの詳細な相関関係を示しています。各行には、特定の脅威と、対応するテスト名、マッピングされたリスク カテゴリ、そしてリスクが最も顕在化する可能性の高い SAIF アーキテクチャ コンポーネント（コンポーネント番号で示す）がリンクされています。

（表）












## 4.5 AI 脅威の AI コンポーネントへのマッピング




## 4.6 参考情報

- [1] National Institute of Standards and Technology (NIST). Artificial Intelligence Risk Management Framework (AI RMF 1.0). NIST Special Publication 1270\. Gaithersburg, MD: U.S. Department of Commerce, January 2023.Available from [https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1270.pdf](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1270.pdf)  
- [2] International Organization for Standardization. ISO/IEC 42001:2022 Information technology, Artificial intelligence, Management system, Requirements. Geneva: ISO, 2022\. Available from [https://www.iso.org/standard/81230.html](https://www.iso.org/standard/81230.html)  
- [3] OWASP Foundation. OWASP Top 10 for Large Language Models (LLMs). OWASP Foundation, 2024\. Available from [https://owasp.org/www-project-top-10-for-large-language-model-applications/](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [4] International Organization for Standardization. ISO/IEC 23053:2021 Information Technology, Framework for Artificial Intelligence (AI) Systems Using Machine Learning (ML). Geneva: ISO, 2021\. Available from [https://www.iso.org/standard/74630.html](https://www.iso.org/standard/74630.html)  
- [5] OWASP Foundation. OWASP AI Exchange. OWASP Foundation, 2024\. Available from [https://owasp.org/www-project-ai-security-and-privacy-guide/](https://owasp.org/www-project-ai-security-and-privacy-guide/)
- [6] NIST SP 800-115. National Institute of Standards and Technology (NIST). Technical Guide to Information Security Testing and Assessment. NIST Special Publication 800-115. Gaithersburg, MD: U.S. Department of Commerce, September 2008\. Available from [https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-115.pdf](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-115.pdf)  
- [7] Institute for Security and Open Methodologies (ISECOM). OSSTMM 3: The Open Source Security Testing Methodology Manual. ISECOM, 2020\. Available from [https://www.isecom.org/research.html#content5-9d](https://www.isecom.org/research.html#content5-9d)
- [8] OWASP Foundation. OWASP Web Security Testing Guide (WSTG) 4.2. OWASP Foundation, 2021\. Available from [https://owasp.org/www-project-web-security-testing-guide/](https://owasp.org/www-project-web-security-testing-guide/)  
- [9] UcedaVélez, T., & Morana, M. M. (2015). *Risk Centric Threat Modeling: Process for Attack Simulation and Threat Analysis*. Wiley. ISBN 978-0-470-50096-5. Available from [https://www.wiley.com/Risk+Centric+Threat+Modeling%3A+Process+for+Attack+Simulation+and+Threat+Analysis-p-9780470500965](https://www.wiley.com/Risk+Centric+Threat+Modeling%3A+Process+for+Attack+Simulation+and+Threat+Analysis-p-9780470500965)
- [10] Shostack, A. (2014). *Threat Modeling: Designing for Security*. Wiley. ISBN 978-1118809990. Available from [https://www.wiley.com/en-us/Threat%2BModeling%3A%2BDesigning%2Bfor%2BSecurity-p-9781118809990](https://www.wiley.com/en-us/Threat%2BModeling%3A%2BDesigning%2Bfor%2BSecurity-p-9781118809990)  
- [11]  MITRE Corporation. (2023). *MITRE ATLAS™:* Adversarial Threat Landscape for Artificial-Intelligence Systems. Retrieved from [https://atlas.mitre.org/](https://atlas.mitre.org/)  
- [12] Wuyts, K., & Joosen, W. (2015). LINDDUN privacy threat modeling: A tutorial (CW Reports CW685). Department of Computer Science, KU Leuven. Retrieved from [https://linddun.org/publications/](https://linddun.org/publications/)  
- [13] Google. (2023). *Secure AI Framework (SAIF): A Conceptual Framework for Secure AI Systems*. Retrieved from [https://safety.google/cybersecurity-advancements/saif/](https://safety.google/cybersecurity-advancements/saif/)  
- [14] *OWASP AI Red Teaming Framework*. Open Worldwide Application Security Project (OWASP), 2024\. Available at: [https://genai.owasp.org/resource/genai-red-teaming-guide/](https://genai.owasp.org/resource/genai-red-teaming-guide/)   
- [15] Lewis, P., Perez, E., Piktus, A., Karpukhin, V., Goyal, N., Küttler, H., … & Riedel, S. (2021). *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks*. In *NeurIPS 2021*. Available from [https://arxiv.org/abs/2005.11401](https://arxiv.org/abs/2005.11401)  
- [16] Angles of Attack Research Group. *Securing AI/ML Systems in the Age of Information Warfare*. Angles of Attack White Paper, 2024\. Available from [https://anglesofattack.io/Securing\_AIML\_Systems\_in\_IW\_Cox.pdf](https://anglesofattack.io/Securing_AIML_Systems_in_IW_Cox.pdf)  
- [17] Scarfone, K., Souppaya, M., Cody, A., & Orebaugh, A. (2008). *Technical Guide to Information Security Testing and Assessment* (NIST Special Publication 800-115). National Institute of Standards and Technology. Retrieved from [https://csrc.nist.gov/publications/detail/sp/800-115/final](https://csrc.nist.gov/publications/detail/sp/800-115/final)  
- [18] Herzog, P., & the Institute for Security and Open Methodologies (ISECOM). (2010). *Open Source Security Testing Methodology Manual (OSSTMM), Version 3*. ISECOM. Retrieved from [https://www.isecom.org/OSSTMM.3.pdf](https://www.isecom.org/OSSTMM.3.pdf)  
- [19]  OWASP Foundation. (2023). *OWASP Web Security Testing Guide (WSTG), Version 4.2*. Open Worldwide Application Security Project. Retrieved from [https://owasp.org/www-project-web-security-testing-guide/](https://owasp.org/www-project-web-security-testing-guide/)  
- [20] Yu, S. (2023). *Cyber Defense Matrix: The Essential Guide to Navigating the Cybersecurity Landscape.* Wiley. ISBN: 978-1119895183. Available from: [https://www.wiley.com/en-us/Cyber+Defense+Matrix%3A+The+Essential+Guide+to+Navigating+the+Cybersecurity+Landscape-p-9781119895183](https://www.wiley.com/en-us/Cyber+Defense+Matrix%3A+The+Essential+Guide+to+Navigating+the+Cybersecurity+Landscape-p-9781119895183)  
- [21] OWASP Agentic Security Initiative. (2025, February 17). *Agentic AI – Threats and Mitigations*. OWASP Generative AI Security Project. Retrieved from [https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/](https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/)  
- [22] OWASP Agentic Security Initiative. *Multi-Agentic System Threat Modeling Guide v1.0.* Retrieved from:
[https://genai.owasp.org/resource/multi-agentic-system-threat-modeling-guide-v1-0/](https/genai.owasp.org/resource/multi-agentic-system-threat-modeling-guide-v1-0/)  
- [23] Jim Hoagland et al. "Prompt Injection Taxonomy for AI Applications." Pangea Security, 2024 (https://pangea.cloud/securebydesign/aiapp-pi-taxonomy/)  
- [24] Ken Huang. “Agentic AI Threat Modeling Framework: MAESTRO (Multi-Agent Environment, Security, Threat, Risk, and Outcome).” Cloud Security Alliance, Feb. 6 2025 (https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro)  
- [25] M. Morana “AI-Powered Threat Modeling – Course Overview.” YouTube, Channel “@CodeRedPR0_Official”, CodeRed Pro. Available at: (https://www.youtube.com/@CodeRedPR0_Official/search?query=powered%20threat%20modeling)  
- [26] M. Morana "LLM Threat Modeling Prompt Templates" Available at: (https://mmorana1.github.io/marcom/trainings/)
