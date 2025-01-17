# コントリビューションガイドライン

Thank you for your interest in contributing to the ML-Agents toolkit! We are
incredibly excited to see how members of our community will use and extend the
ML-Agents toolkit. To facilitate your contributions, we've outlined a brief set
of guidelines to ensure that your extensions can be easily integrated.
ML-Agentsツールキットへの貢献に関心をお寄せいただきありがとうございます！ 私たちのコミュニティのメンバーが、どのようにML-Agentsツールキットを使用しまた拡張するのかを見ることは、とてもエキサイティングなことです。 あなたの貢献を促進し、あなたの拡張が容易に統合されることができることを確実にするために、私達はガイドラインの簡単なセットを概説しました。

## Communication

First, please read through our [code of conduct](CODE_OF_CONDUCT.md), as we
expect all our contributors to follow it.

Second, before starting on a project that you intend to contribute to the
ML-Agents toolkit (whether environments or modifications to the codebase), we
**strongly** recommend posting on our
[Issues page](https://github.com/Unity-Technologies/ml-agents/issues)
and briefly outlining the changes you plan to make. This will enable us to
provide some context that may be helpful for you. This could range from advice
and feedback on how to optimally perform your changes or reasons for not doing
it.

Lastly, if you're looking for input on what to contribute, feel free to
reach out to us directly at ml-agents@unity3d.com and/or browse the GitHub
issues with the `contributions welcome` label.

## Git Branches

Starting with v0.3, we adopted the
[Gitflow Workflow](http://nvie.com/posts/a-successful-git-branching-model/).
Consequently, the `master` branch corresponds to the latest release of
the project, while the `develop` branch corresponds to the most recent, stable,
version of the project.

Thus, when adding to the project, **please branch off `develop`**
and make sure that your Pull Request (PR) contains the following:

* Detailed description of the changes performed
* Corresponding changes to documentation, unit tests and sample environments (if
  applicable)
* Summary of the tests performed to validate your changes
* Issue numbers that the PR resolves (if any)

## Environments

We are also actively open to adding community contributed environments as
examples, as long as they are small, simple, demonstrate a unique feature of
the platform, and provide a unique non-trivial challenge to modern
machine learning algorithms. Feel free to submit these environments with a
PR explaining the nature of the environment and task.

## Style Guide

When performing changes to the codebase, please ensure that all python code is reformatted using the [black](https://github.com/ambv/black) formatter. For C#, we will soon be requirements for style and formatting.
