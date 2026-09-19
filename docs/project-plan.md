# 项目规划与资源需求 / Project plan and resource estimates

状态：筹备中。本文描述拟开展的工作，并非已完成成果或交付时限承诺。

Status: planning stage. This document describes proposed work, not completed deliverables or delivery deadlines.

## 目标与首批内容 / Goal and initial scope

将维护者已有的服务器、容器和自动化实践整理为免费公开、可复现的学习材料。每份教程说明环境、步骤、验证、常见问题和回滚方式。

Turn the maintainer's existing server, container and automation experience into free, reproducible learning materials. Each guide should document its environment, steps, verification, known issues and rollback.

首批拟整理的主题 / Proposed initial topics:

1. Linux 服务与 Docker 容器的只读状态检查 / Read-only Linux service and Docker container checks.
2. 一个最小 Docker 部署示例及验证、清理说明 / A minimal Docker deployment example with verification and cleanup instructions.
3. 配套脚本与故障排查记录 / Supporting scripts and troubleshooting notes.
4. 资源允许时整理 Ollama 小型量化模型实验 / Optional small quantized-model experiments with Ollama, subject to available resources.

这些主题尚未实现或完成测试。文档可先通过 GitHub 免费公开；服务器主要用于后续演示和运行验证，不是发布文档的前提。

These topics have not yet been implemented or tested. Documentation can be published on GitHub before server allocation; infrastructure would primarily support later demonstrations and runtime validation.

## 基础设施估算 / Infrastructure estimates

| 项目 / Item | 基础配置 / Baseline | 可选独服配置 / Optional dedicated server |
|---|---|---|
| CPU | 4 vCPU，接受 VPS / VPS acceptable | 约 4 个物理核心 / Around 4 physical cores |
| 内存 / RAM | 8 GB | 16 GB |
| SSD | 100 GB | 200 GB |
| 系统 / OS | Ubuntu 24.04 LTS 或合适的 Linux 发行版 / Or another suitable Linux distribution | 同左 / Same |
| 网络 / Network | 100 Mbps 端口；初期暂按每月不超过 300 GB 规划 / 100 Mbps port; initial estimate up to 300 GB per month | 同左 / Same |
| GPU | 不要求 / Not required | 不要求 / Not required |

基础配置用于文档站、少量 Docker 示例和按需脚本验证。较大配置仅为有限的小模型 CPU 实验提供余量；独服不是启动项目的必要条件。初期文档和最小示例可以从更小配置开始，按实测情况调整。

The baseline would support a documentation site, a few Docker examples and on-demand script validation. The larger option adds room for limited small-model CPU experiments; a dedicated server is not required to start the project. Initial documentation and minimal examples can begin with smaller resources and be adjusted based on measurements.

预期以低并发文档访问为主，验证或模型实验期间负载短时升高。模型实验计划每次仅运行一个小型量化模型，具体是否可行取决于模型、量化方式和上下文长度。项目不计划大模型训练或高并发公共推理服务。

Expected workload is mostly low-concurrency documentation access, with temporary load increases during validation or experiments. Model experiments would run one small quantized model at a time; feasibility depends on the model, quantization and context length. Large-model training and high-concurrency public inference are outside the planned scope.

以上数字仅为规划估算，尚无线上访问或性能测试数据，不代表供应商承诺或已获批资源。

These figures are planning estimates. There are no production traffic measurements or benchmark results, and no provider allocation or commitment is implied.

## 维护与公开方式 / Maintenance and publication

计划免费公开有权发布的教程、脚本和配置示例，保留第三方许可说明。每次发布应记录测试环境和结果；缺少验证时明确标注，不把计划内容写成可用功能。

The project plans to publish tutorials, scripts and configurations it has the right to distribute, preserving third-party licensing notices. Releases should record the test environment and results; unverified material must be labeled and planned work must not be presented as available functionality.

如未来获得服务器支持，将依据支持计划配合活跃状态核查；项目停止维护时通知提供方。当前没有已确认的服务器或赞助合作。

If infrastructure support is granted, the project will follow the program's activity review process and notify the provider if maintenance stops. There is currently no confirmed server allocation or sponsorship.
