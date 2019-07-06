<img src="docs/images/unity-wide.png" align="middle" width="3000"/>

<img src="docs/images/image-banner.png" align="middle" width="3000"/>

# Unity ML-Agents ツールキット (ベータ)
[![docs badge](https://img.shields.io/badge/docs-reference-blue.svg)](docs/Readme.md)
[![license badge](https://img.shields.io/badge/license-Apache--2.0-green.svg)](LICENSE)

**The Unity Machine Learning Agents ツールキット** （ML-Agents）は、ゲームやシミュレーションが知的エージェントを訓練するための環境として機能することを可能にするオープンソースのUnityプラグインです。 エージェントは、強化学習、模倣学習、ニューロ進化、または使いやすいPython APIによる他の機械学習方法を使用してトレーニングできます。 また、ゲーム開発者や愛好家が2D、3D、VR / ARゲーム用のインテリジェントエージェントを簡単にトレーニングできるようにするための最先端のアルゴリズムの実装（TensorFlowに基づく）も提供しています。 これらの訓練されたエージェントは、（マルチエージェントや敵対者のような様々な設定における）NPCの振る舞いの制御、ゲームビルドの自動テスト、そしてリリース前のさまざまなゲームデザインの決定の評価などの目的に使用できます。 ML-Agentsツールキットは、AIの進歩をUnityの豊かな環境で評価してから、幅広い研究開発者やゲーム開発者コミュニティにアクセスできるようにするためのセントラルプラットフォームであり、ゲーム開発者とAI研究者の双方にとって有益です。
## 特徴


* PythonからのUnity環境制御
* 10+サンプルのUnity環境
* 複数の環境構成とトレーニングシナリオのサポート
* 深層強化学習を使用した記憶力強化エージェントの訓練
* 簡単に定義可能なカリキュラム学習シナリオ
* 教師付き学習のためのエージェント行動のブロードキャスト
* 模造学習のための組み込みサポート
* オンデマンド意思決定による柔軟なエージェント制御
* 環境内のネットワーク出力を視覚化する
* Dockerを使った簡単な設定
* ジムとして学習環境をラップ
* Unity推論エンジンを利用する
* コンカレントUnity環境インスタンスを使用したトレーニング


## ドキュメンテーション

* 詳細については、インストールと使用方法の説明に加えて、[documentation home](docs/Readme.md)を参照してください。  
* あなたがAIプラットフォームとしてのUnityの議論に興味を持っている研究者であれば、私たちの[UnityとML-Agents Toolkitに関するリファレンスペーパー](https://arxiv.org/abs/1809.02627)のプレプリントを見てください。 また、このホワイトペーパーを引用する手順については、以下を参照してください。  
* 以前のバージョンのML-Agentsツールキットを使用したことがある場合は、[以前のバージョンからの移行に関するガイド](docs/Migrating.md)を参照することを強くお勧めします。


## 追加のリソース

ML-Agentsに関連する一連のブログ記事を公開しました。

*強化学習の概念の概要
  （[マルチ武装盗賊](https://blogs.unity3d.com/2017/06/26/unity-ai-themed-blog-entries/)
  そして
  [Q-learning](https://blogs.unity3d.com/2017/08/22/unity-ai-reinforcement-learning-with-q-learning/))
* [実際のゲームでの機械学習エージェントの使用：初心者ガイド](https://blogs.unity3d.com/2017/12/11/using-machine-learning-agents-in-a-real-game-a-beginners-guide/)
* [投稿](https://blogs.unity3d.com/2018/02/28/introducing-the-winners-of-the-first-ml-agents-challenge/)
  私たちの勝者を発表
  [最初のML-Agentsチャレンジ](https://connect.unity.com/challenges/ml-agents-1)
* [投稿](https://blogs.unity3d.com/2018/01/23/designing-safer-cities-through-simulations/)
  より安全な都市をデザインするためのシミュレータとしてUnityをどのように活用できるかを概説します。

私たち自身のドキュメンテーションに加えて、ここにいくつかの追加の関連記事があります：

* [Unity AI  -  Unity 3D人工知能](https://www.youtube.com/watch?v=bqsfkGbBU6k)
* [ゲーム開発者が機械学習を学ぶ](https://mikecann.co.uk/machine-learning/a-game-developer-learns-machine-learning-intent/)
* [インテルアーキテクチャ専用のUnity Technologies ML-Agentsについて](https://software.intel.com/en-us/articles/explore-unity-technologies-ml-agents-exclusively-on-intel-architecture)

## コミュニティとフィードバック

ML-Agentsツールキットはオープンソースプロジェクトであり、私たちは貢献を奨励し歓迎します。 あなたが貢献したいならば、必ず私たちの[貢献ガイドライン]（CONTRIBUTING.md）と[行動規範]（CODE_OF_CONDUCT.md）を見直してください。

ML-Agentsツールキットを使用して問題が発生した場合は、[issueを送信してください](https://github.com/Unity-Technologies/ml-agents/issues) 、可能な限り詳細を含めるようにしてください。

あなたの意見は私達にとって非常に重要です。 Unity ML-Agents Toolkitについてのあなたの考えを聞くことによってのみ、私たちは改善し成長し続けることができます。私たちに知らせるために、どうか数分でよいのでお時間をください[それについて教えてください](https://github.com/Unity-Technologies/ml-agents/issues/1454). 

その他の質問やフィードバックについては、ML-Agentsチーム（ml-agents@unity3d.com）に直接連絡してください。
## 翻訳

Unity ML-Agentsツールキットを世界の研究コミュニティおよびUnity開発者コミュニティが利用できるようにするために、私たちはドキュメントの翻訳を作成し、維持しようとしています。 ドキュメントのサブセットを1つの言語（中国語）に翻訳することから始めましたが、もっと多くのページや他の言語に翻訳し続けることを望みます。 ゆえに私たちは、コミュニティからのあらゆる強化そして改善を歓迎します。

* [中国語](docs/localized/zh-CN/)

## ライセンス

[Apache License 2.0](LICENSE)

## 引用

UnityまたはML-Agentsツールキットを使用して研究を行う場合は、以下の論文をリファレンスにしてください。

Juliani, A., Berges, V., Vckay, E., Gao, Y., Henry, H., Mattar, M., Lange, D. (2018). Unity: A General Platform for Intelligent Agents. *arXiv preprint arXiv:1809.02627.* https://github.com/Unity-Technologies/ml-agents.
