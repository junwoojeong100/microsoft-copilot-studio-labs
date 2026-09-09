# Copilot Studio Hands-on Labs

[English](README.md) | [한국어](README.ko.md)

Build a Copilot Studio agent, configure its knowledge and tools, and confirm its behavior using the same assets. This repository contains two self-contained HTML guides and four recorded walkthroughs, separated into **Create** and **Use**.

**English is the default documentation language.** Korean editions are also included.

📖 **Read the guides online — no download required:** <https://junwoojeong100.github.io/microsoft-copilot-studio-labs/>

## Choose a guide

| Guide | Intended audience and outcome | English | 한국어 |
|---|---|---|---|
| Beginner | Business users and first-time makers: a synthetic HR FAQ agent, grounded answers, leave-request input validation, and personal Teams use | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.html) | [가이드 열기](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.ko.html) |
| Azure developer | Developers: REST APIs, Foundry models, MCP, Foundry IQ retrieval, and approval workflows with explicit authentication and execution evidence | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.html) | [가이드 열기](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.ko.html) |

The beginner core path is **L01 → L02 → L03 → L09**. For the developer guide, complete **Lab 0: base-agent preparation** before the five core labs **L04 → L05 → L12 → L14 → L20**. Lab 0 is a preparatory step, not an additional core completion item. **L08 Foundry Agent** is an additional optional/preview lab included in the developer recordings.

The developer guide assumes familiarity with the beginner concepts but includes its own minimal agent setup. Completing the beginner guide does not imply completion of the developer guide. A detailed comparison is available in each guide's reference appendix.

## Recorded walkthroughs

| Guide | Create | Use |
|---|---|---|
| Beginner | [4 min 33 sec](copilot-studio-hands-on-lab-create-20260909.mp4) | [3 min 21 sec](copilot-studio-hands-on-lab-use-20260909.mp4) |
| Azure developer | [10 min 28 sec](copilot-studio-lab-for-azure-devs-create-20260909.mp4) | [9 min 21 sec](copilot-studio-lab-for-azure-devs-use-20260909.mp4) |

Both language editions use the same **Korean-captioned videos with Korean lab prompts and responses**. These are edited walkthroughs using fictional data.

The HTML guides include chapter timestamps. Video duration is not the time required to perform the labs; approval, provisioning, indexing, and publication delays are separate.

## Open the guides

No build or package installation is required for the documentation.

**Online — GitHub Pages.** Use the links in [Choose a guide](#choose-a-guide). Videos are served from the same site.

**Offline — local copy.**

1. Download or clone the repository.
2. Open either HTML guide in a modern browser, keeping the MP4 files in the same directory.
3. Follow **Create** first, retain the generated assets, and then follow **Use** with the same saved configuration.

If local-file browser restrictions affect clipboard or other interactions, serve the directory locally:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open:

- Beginner: <http://127.0.0.1:8000/copilot-studio-hands-on-lab.html>
- Developer: <http://127.0.0.1:8000/copilot-studio-lab-for-azure-devs.html>

GitHub's file viewer displays HTML source rather than the interactive guide, so use the GitHub Pages links above. If you fork or re-host the repository, preserve the relative filenames so language switches and video links continue to work.

## Language and reproducibility

Copy executable snippets, identifiers, and Korean input/status values exactly as shown. English explanations beside the samples describe their meaning; do not substitute the translations for literal inputs. Replace placeholders such as `<LAB_PREFIX>` using the naming rules in each guide's prerequisites.

The **English / 한국어** switch in each guide opens the corresponding language edition. Progress checkboxes are a local convenience, not evidence that a cloud operation succeeded.

## Prerequisites and safety

- Use an approved non-production Sandbox, the appropriate maker permissions, and the required product licenses or credits. Signing in alone does not establish those rights.
- Azure-dependent labs require approved external resources, connections, Microsoft Entra authentication, and least-privilege RBAC. These are not provisioned merely by opening the HTML.
- Use only synthetic data and the approved self-test recipient/approver. Do not submit real HR requests, make payments, or send test approvals to other people.
- Environment-specific resource names and IDs are examples. Adapt them to your own approved environment. **Confirm ownership and dependencies before deleting lab resources.**
- Never commit API keys, tokens, credentials, or personal data. Stop lab workflows and clear pending test approvals when finished; shared resources must not be deleted indiscriminately.

## Important integration boundaries

| Area | What these materials demonstrate |
|---|---|
| Foundry Model | Native BYOM through an API Management endpoint; APIM uses managed identity for the model backend. An APIM subscription key is not a Foundry API key. |
| Foundry Agent | Optional/preview native delegation using the Activity protocol and a prepared Foundry agent. |
| Foundry IQ | A verified custom MCP route through APIM's HTTP proxy. This is not proof that the native Foundry IQ connector works, nor that Consumption supports dedicated MCP-server import. |
| Approval workflow | Intake, actual record ID, input rejection, automatic approval, and self-test approval/rejection. The actual output key/type and ID interpretation are documented. Automatic expiration is optional and not claimed as verified. |

UI, availability, licensing, and preview status can vary by tenant and change over time. Use the dates, prerequisites, official references, and completion criteria in each guide; a connection badge or HTTP 200 alone is not an end-to-end success criterion.
