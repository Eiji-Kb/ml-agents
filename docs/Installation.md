# インストール

ML-Agentsをインストールして使用するには、Unityをインストールし、このリポジトリを複製し、そしてPythonを追加の依存関係と共にインストールする必要があります。 以下の各サブセクションでは、Dockerの設定に加えて、各ステップの概要を説明します。

## **Unity 2017.4** 以降をインストール

[ダウンロード](https://store.unity.com/download) してUnityをインストールしてください。Dockerセットアップ（後で紹介します）を使用したい場合は、Unityのインストール時に _Linux Build Support_ コンポーネントを必ず選択してください。

<p align="center">
  <img src="images/unity_linux_build_support.png"
       alt="Linux Build Support"
       width="500" border="10" />
</p>

## Windows ユーザ
For setting up your environment on Windows, we have created a [detailed
guide](Installation-Windows.md) to setting up your env. For Mac and Linux,
continue with this guide.
Windowsであなたの環境をセットアップするために、私達はあなたの環境をセットアップするために[詳細ガイド](Installation-Windows.md) を作成しました。 （MacとLinuxの場合は、このままこのガイドを続けてください。）

## Mac and Unix Users

### ML-Agents ツールキット リポジトリのクローン作成

Once installed, you will want to clone the ML-Agents Toolkit GitHub repository.
インストールが完了したら、ML-Agents ツールキット GitHubリポジトリを複製します。

```sh
git clone https://github.com/Unity-Technologies/ml-agents.git
```

The `UnitySDK` subdirectory contains the Unity Assets to add to your projects.
It also contains many [example environments](Learning-Environment-Examples.md)
to help you get started.

The `ml-agents` subdirectory contains a Python package which provides deep reinforcement 
learning trainers to use with Unity environments.

The `ml-agents-envs` subdirectory contains a Python API to interface with Unity, which
the `ml-agents` package depends on. 

The `gym-unity` subdirectory contains a package to interface with OpenAI Gym.

`UnitySDK`サブディレクトリはあなたのプロジェクトに追加するUnityアセットを含みます。
それはまたあなたが始めるのを助けるために多くの[サンプル環境]（Learning-Environment-Examples.md）を含んでいます。

`ml-agents`サブディレクトリには、Unity環境で使用するための深層強化学習トレーナーを提供するPythonパッケージが含まれています。

`ml-agents-envs`サブディレクトリはUnityとインターフェースをとるためのPython APIを含んでいます。これは` ml-agents`パッケージが依存しています。

`gym-unity`サブディレクトリはOpenAI Gymとインターフェースをとるためのパッケージを含みます。

### Pythonとmlagentsパッケージをインストールする

In order to use ML-Agents toolkit, you need Python 3.6 along with the
dependencies listed in the [setup.py file](../ml-agents/setup.py).
Some of the primary dependencies include:
ML-Agentsツールキットを使用するには、[setup.pyファイル]（../ ml-agents / setup.py）にリストされている依存関係と共にPython 3.6が必要です。
主な依存関係には、次のものがあります。


- [TensorFlow](Background-TensorFlow.md) (Requires a CPU w/ AVX support)
- [Jupyter](Background-Jupyter.md)
- [TensorFlow](Background-TensorFlow.md)（AVXサポート付きのCPUが必要）
- [Jupyter](Background-Jupyter.md)

[Download](https://www.python.org/downloads/) and install Python 3.6 if you do not
already have it.
99/5000
[ダウンロード]（https://www.python.org/downloads/）していなければPython 3.6をインストールしてください。

If your Python environment doesn't include `pip3`, see these
[instructions](https://packaging.python.org/guides/installing-using-linux-tools/#installing-pip-setuptools-wheel-with-linux-package-managers)
on installing it.

Python環境に `pip3`が含まれていない場合は、以下の[手順]を参照してください（https://packaging.python.org/guides/installation-using-linux-tools/#installing-pip-setuptools-wheel-with-linux）  - パッケージマネージャ）
それをインストールする。

To install the dependencies and `mlagents` Python package, run from the command line:
依存関係と `mlagents` Pythonパッケージをインストールするには、コマンドラインから実行してください。

```sh
pip3 install mlagents
```

Note that this will install `ml-agents` from PyPi, _not_ from the cloned repo. 
If you installed this correctly, you should be able to run
`mlagents-learn --help`, after which you will see the Unity logo and the command line
parameters you can use with `mlagents-learn`. 

これはPyPiから `ml-agents`をインストールし、クローンレポジトリからはインストールしません。 これを正しくインストールすれば、 `mlagents-learn --help`を実行できるはずです。その後、Unityロゴと` mlagents-learn`で使用できるコマンドラインパラメータが表示されます。

**Notes:**

- We do not currently support Python 3.7 or Python 3.5.
- If you are using Anaconda and are having trouble with TensorFlow, please see
  the following
  [link](https://www.tensorflow.org/install/pip)
  on how to install TensorFlow in an Anaconda environment.

### Installing for Development

If you intend to make modifications to `ml-agents` or `ml-agents-envs`, you should install 
the packages from the cloned repo rather than from PyPi. To do this, you will need to install
 `ml-agents` and `ml-agents-envs` separately. From the repo's root directory, run:
 
 - 現在、Python 3.7またはPython 3.5はサポートされていません。
 -  Anacondaを使用していてTensorFlowで問題がある場合は、Anaconda環境でTensorFlowをインストールする方法について、以下の[リンク]（https://www.tensorflow.org/install/pip）を参照してください。
 
```sh
cd ml-agents-envs
pip3 install -e ./
cd ..
cd ml-agents
pip3 install -e ./
```

Running pip with the `-e` flag will let you make changes to the Python files directly and have those
reflected when you run `mlagents-learn`. It is important to install these packages in this order as the
`mlagents` package depends on `mlagents_envs`, and installing it in the other 
order will download `mlagents_envs` from PyPi. 

`-e`フラグを付けてpipを実行すると、Pythonファイルに直接変更を加えることができ、` mlagents-learn`を実行したときに反映されます。 `mlagents`パッケージは` mlagents_envs`に依存しており、他の順番でインストールするとPyPiから `mlagents_envs`をダウンロードするので、これらのパッケージをこの順番でインストールすることが重要です。

## Docker-based Installation

If you'd like to use Docker for ML-Agents, please follow
[this guide](Using-Docker.md).


ML-AgentsにDockerを使用したい場合は、次の手順に従ってください。
[このガイド]（Using-Docker.md）。
## Next Steps

The [Basic Guide](Basic-Guide.md) page contains several short tutorials on
setting up the ML-Agents toolkit within Unity, running a pre-trained model, in
addition to building and training environments.
[基本ガイド]（Basic-Guide.md）ページには、Unity内でML-Agentsツールキットをセットアップし、事前に訓練されたモデルを実行して、環境を構築したり訓練したりするための短いチュートリアルがいくつか含まれています。

## Help

If you run into any problems regarding ML-Agents, refer to our [FAQ](FAQ.md) and
our [Limitations](Limitations.md) pages. If you can't find anything please
[submit an issue](https://github.com/Unity-Technologies/ml-agents/issues) and
make sure to cite relevant information on OS, Python version, and exact error
message (whenever possible).

ML-Agentsに関して何か問題が発生した場合は、[FAQ]（FAQ.md）および[制限]（Limitations.md）のページを参照してください。 見つからない場合は[issueを送信]（https://github.com/Unity-Technologies/ml-agents/issues）し、OS、Pythonのバージョン、正確なエラーメッセージに関する関連情報を必ず引用してください（ いつでも可能なとき）。
