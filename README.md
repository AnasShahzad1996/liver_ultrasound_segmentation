<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![PyPi][pypi-shield]][pypi-url]
[![Contributors][contributors-shield]][contributors-url]
[![License][license-shield]][license-url]
<!-- [![Build][build-shield]][build-url] -->
<!-- [![CodeCov][codecov-shield]][codecov-url] -->

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[pypi-shield]: https://img.shields.io/pypi/pyversions/zenml?style=for-the-badge

[pypi-url]: https://pypi.org/project/zenml/

[pypiversion-shield]: https://img.shields.io/pypi/v/zenml?style=for-the-badge

[downloads-shield]: https://img.shields.io/pypi/dm/zenml?style=for-the-badge

[downloads-url]: https://pypi.org/project/zenml/

[codecov-shield]: https://img.shields.io/codecov/c/gh/zenml-io/zenml?style=for-the-badge

[codecov-url]: https://codecov.io/gh/zenml-io/zenml

[contributors-shield]: https://img.shields.io/github/contributors/zenml-io/zenml?style=for-the-badge

[contributors-url]: https://github.com/AnasShahzad1996/liver_ultrasound_segmentation/graphs/contributors

[license-shield]: https://img.shields.io/github/license/zenml-io/zenml?style=for-the-badge

[license-url]: https://github.com/zenml-io/zenml/blob/main/LICENSE

[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555

[linkedin-url]: https://www.linkedin.com/company/zenml/

[twitter-shield]: https://img.shields.io/twitter/follow/zenml_io?style=for-the-badge

[twitter-url]: https://twitter.com/zenml_io

[slack-shield]: https://img.shields.io/badge/-Slack-black.svg?style=for-the-badge&logo=linkedin&colorB=555

[slack-url]: https://zenml.io/slack-invite

[build-shield]: https://img.shields.io/github/workflow/status/zenml-io/zenml/Build,%20Lint,%20Unit%20&%20Integration%20Test/develop?logo=github&style=for-the-badge

[build-url]: https://github.com/zenml-io/zenml/actions/workflows/ci.yml


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://www.cs.cit.tum.de/camp/start/">
    <img alt="ZenML Logo" src="https://github.com/AnasShahzad1996/liver_ultrasound_segmentation/blob/master/utils/logo.png" alt="Logo" width="400">
  </a>

<h3 align="center">Ultrasound image segmentation</h3>

  <p align="center">
    This repository contains code to segment ultra-sound images using SOTA self-supervised methods
    <br />
    <a href="https://github.com/AnasShahzad1996/liver_ultrasound_segmentation/issues">Report Bug</a>
    ·
    <a href="#-meet-the-team">Meet the Team</a>
    <br />
    🎉 Version 0.1.0 is out. Release notes to be updated soon
    <a href="https://github.com/AnasShahzad1996/liver_ultrasound_segmentation/wiki">here</a>.
    <br />
    <br />
    <a href="https://www.linkedin.com/company/tum-camp/?originalSubdomain=de">
    <img src="https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555" alt="Logo">
    </a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>🏁 Table of Contents</summary>
  <ol>
    <li><a href="#-introduction">Introduction</a></li>
    <li><a href="#-quickstart">Install requirements</a></li>
    <li>
      <a href="#-create-your-own-mlops-platform">Download the ultra-sound dataset</a></li>
    <li><a href="#-roadmap">Literature Review</a></li>
    <li><a href="#-contributing-and-community">Models and models</a></li>
    <li><a href="#-getting-help">Getting Help</a></li>
    <li><a href="#-license">License</a></li>
  </ol>
</details>

<br />

# 🤖 Introduction

🤹 ZenML is an extensible, open-source MLOps framework for creating portable,
production-ready machine learning pipelines. By decoupling infrastructure from
code, ZenML enables developers across your organization to collaborate more
effectively as they develop to production.

- 💼 ZenML gives data scientists the freedom to fully focus on modeling and
experimentation while writing code that is production-ready from the get-go.

- 👨‍💻 ZenML empowers ML engineers to take ownership of the entire ML lifecycle
  end-to-end. Adopting ZenML means fewer handover points and more visibility on
  what is happening in your organization.

- 🛫 ZenML enables MLOps infrastructure experts to define, deploy, and manage
sophisticated production environments that are easy to use for colleagues.

![The long journey from experimentation to production.](/docs/book/.gitbook/assets/intro-zenml-overview.png)

ZenML provides a user-friendly syntax designed for ML workflows, compatible with
any cloud or tool. It enables centralized pipeline management, enabling
developers to write code once and effortlessly deploy it to various
infrastructures.

<div align="center">
    <img src="docs/book/.gitbook/assets/stack.gif">
</div>

# 🤸 Install requirements

[Install ZenML](https://docs.zenml.io/getting-started/installation) via
[PyPI](https://pypi.org/project/zenml/). Python 3.7 - 3.10 is required:

```bash
conda create --name liver_segmentation
conda activate liver_segmentation
pip install -r requirements.txt
```

# 🖼️ Download the ultra-sound dataset

ZenML allows you to create and manage your own MLOps platform using 
best-in-class open-source and cloud-based technologies. Here is an example of 
how you could set this up for your team:

## 🔋 1. Deploy ZenML

For full functionality ZenML should be deployed on the cloud to
enable collaborative features as the central MLOps interface for teams.

![ZenML Architecture Diagram.](docs/book/.gitbook/assets/Scenario3.png)

In case your machine is authenticated with one of the big three cloud 
providers, this command will do the full deployment for you.

```bash
zenml deploy --provider aws  # aws, gcp and azure are supported providers
```

You can also choose to deploy with docker or helm with full control over
the configuration and deployment. Check out the
[docs](https://docs.zenml.io/platform-guide/set-up-your-mlops-platform/deploy-zenml)
to find out how.

## 👨‍🍳 2. Deploy Stack Components

ZenML boasts a ton of [integrations](https://zenml.io/integrations) into 
popular MLOps tools. The [ZenML Stack](https://docs.zenml.io/user-guide/starter-guide/understand-stacks) 
concept ensures that these tools work nicely together, therefore bringing
structure and standardization into the MLOps workflow.

Deploying and configuring this is super easy with ZenML. For **AWS**, this might 
look a bit like this

```bash
# Deploy and register an orchestrator and an artifact store
zenml orchestrator deploy kubernetes_orchestrator --flavor kubernetes --cloud aws
zenml artifact-store deploy s3_artifact_store --flavor s3

# Register this combination of components as a stack
zenml stack register production_stack --orchestrator kubernetes_orchestrator --artifact-store s3_artifact_store --set # Register your production environment
```

When you run a pipeline with this stack set, it will be running on your deployed
Kubernetes cluster.

You can also [deploy your own tooling manually](https://docs.zenml.io/platform-guide/set-up-your-mlops-platform/deploy-and-set-up-a-cloud-stack)
or [**create your own MLOps Platform Sandbox**](https://docs.zenml.io/user-guide/advanced-guide/sandbox), 
a one-click deployment platform for an ephemeral MLOps stack that you can use 
to run production-ready MLOps pipelines in the cloud.

## 🏇 3. Create a Pipeline

Here's an example of a hello world ZenML pipeline in code:

```python
# run.py
from zenml import pipeline, step


@step
def step_1() -> str:
    """Returns the `world` substring."""
    return "world"


@step
def step_2(input_one: str, input_two: str) -> None:
    """Combines the two strings at its input and prints them."""
    combined_str = input_one + ' ' + input_two
    print(combined_str)


@pipeline
def my_pipeline():
    output_step_one = step_1()
    step_2(input_one="hello", input_two=output_step_one)


if __name__ == "__main__":
    my_pipeline()
```

```bash
python run.py
```

## 👭 4. Start the Dashboard

Open up the ZenML dashboard using this command.

```bash
zenml show
```

![ZenML Dashboard](docs/book/.gitbook/assets/landingpage.png)

# 🗺 Roadmap

ZenML is being built in public. The [roadmap](https://zenml.io/roadmap) is a
regularly updated source of truth for the ZenML community to understand where
the product is going in the short, medium, and long term.

ZenML is managed by a [core team](https://zenml.io/company#CompanyTeam) of
developers that are responsible for making key decisions and incorporating
feedback from the community. The team oversees feedback via various channels,
and you can directly influence the roadmap as follows:

- Vote on your most wanted feature on our [Discussion
  board](https://zenml.io/discussion).
- Start a thread in our [Slack channel](https://zenml.io/slack-invite).
- [Create an issue](https://github.com/zenml-io/zenml/issues/new/choose) on our
  Github repo.

# 🙌 Contributing and Community

We would love to develop ZenML together with our community! Best way to get
started is to select any issue from the [`good-first-issue`
label](https://github.com/zenml-io/zenml/labels/good%20first%20issue). If you
would like to contribute, please review our [Contributing
Guide](CONTRIBUTING.md) for all relevant details.

# 🆘 Getting Help

The first point of call should
be [our Slack group](https://zenml.io/slack-invite/).
Ask your questions about bugs or specific use cases, and someone from
the [core team](https://zenml.io/company#CompanyTeam) will respond.
Or, if you
prefer, [open an issue](https://github.com/zenml-io/zenml/issues/new/choose) on
our GitHub repo.

# 📜 License

ZenML is distributed under the terms of the Apache License Version 2.0.
A complete version of the license is available in the [LICENSE](LICENSE) file in
this repository. Any contribution made to this project will be licensed under
the Apache License Version 2.0.
