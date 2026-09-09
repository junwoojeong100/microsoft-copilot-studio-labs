# Copilot Studio Hands-on Labs

[English](README.md) | [한국어](README.ko.md)

Build a Copilot Studio agent, configure its knowledge and tools, and confirm its behavior using the same assets. This repository contains two self-contained HTML guides and four recorded walkthroughs, separated into **Create** and **Use**.

**English is the default documentation language.** The Korean editions are also included. Both editions link to the same original recordings.

📖 **Read the guides online — no download required:** <https://junwoojeong100.github.io/microsoft-copilot-studio-labs/>

## Choose a guide

| Guide | Intended audience and outcome | English | 한국어 |
|---|---|---|---|
| Beginner | Business users and first-time makers: a synthetic HR FAQ agent, grounded answers, leave-request input validation, and personal Teams use | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.html) | [가이드 열기](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.ko.html) |
| Azure developer | Developers: REST APIs, Foundry models, MCP, Foundry IQ retrieval, and approval workflows with explicit authentication and execution evidence | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.html) | [가이드 열기](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.ko.html) |

The beginner core path is **L01 → L02 → L03 → L09**. The developer core path is **L04 → L05 → L12 → L14 → L20**; **L08 Foundry Agent** is an additional optional/preview lab included in the developer recordings.

The developer guide assumes familiarity with the beginner concepts but includes its own minimal agent setup. Completing the beginner guide does not imply completion of the developer guide. A comparison table near the beginning of each guide explains the difference.

## Recorded walkthroughs

| Guide | Create | Use |
|---|---|---|
| Beginner | [4 min 33 sec](copilot-studio-hands-on-lab-create-20260909.mp4) | [3 min 21 sec](copilot-studio-hands-on-lab-use-20260909.mp4) |
| Azure developer | [10 min 28 sec](copilot-studio-lab-for-azure-devs-create-20260909.mp4) | [9 min 21 sec](copilot-studio-lab-for-azure-devs-use-20260909.mp4) |

These are the **original recordings with Korean captions, lab prompts, and responses**. They have not been translated, dubbed, or replaced for the English guides. The videos are edited from actual screen recordings: waiting periods and unsuccessful interaction windows are shortened or omitted, and some real frames are held for readability. They are not uninterrupted one-take recordings.

The HTML guides include chapter timestamps. Video duration is not the time required to perform the labs; approval, provisioning, indexing, and publication delays are separate.

## Open the guides

No build or package installation is required for the documentation.

**Online — GitHub Pages.** Open a published guide directly, with the videos streamed from the same site:

- Beginner: <https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.html>
- Developer: <https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.html>

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

English guide explanations, navigation, tables, and accessibility text are translated. Executable snippets, identifiers, and recorded Korean input/status values are retained where necessary to preserve the lab contracts and match the recordings. The surrounding English explanations describe how to use these samples.

The **English / 한국어** switch in each guide opens the corresponding language edition. Progress checkboxes are a local convenience, not evidence that a cloud operation succeeded.

## Prerequisites and safety

- Use an approved non-production Sandbox, the appropriate maker permissions, and the required product licenses or credits. Signing in alone does not establish those rights.
- Azure-dependent labs require approved external resources, connections, Microsoft Entra authentication, and least-privilege RBAC. These are not provisioned merely by opening the HTML.
- Use only synthetic data and the approved self-test recipient/approver. Do not submit real HR requests, make payments, or send test approvals to other people.
- Environment-specific resource names and IDs are examples from the recorded lab. Adapt them to your own approved environment. **Review cleanup commands before running them: they can delete resources.**
- Never commit API keys, tokens, credentials, or personal data. Stop lab workflows and clear pending test approvals when finished; shared resources must not be deleted indiscriminately.

## Important integration boundaries

| Area | What these materials demonstrate |
|---|---|
| Foundry Model | Native BYOM through an API Management endpoint; APIM uses managed identity for the model backend. An APIM subscription key is not a Foundry API key. |
| Foundry Agent | Optional/preview native delegation using the Activity protocol and a prepared Foundry agent. |
| Foundry IQ | A verified custom MCP route through APIM's HTTP proxy. This is not proof that the native Foundry IQ connector works, nor that Consumption supports dedicated MCP-server import. |
| Approval workflow | Intake, actual record ID, input rejection, automatic approval, and self-test approval/rejection. The actual output key/type and ID interpretation are documented. Automatic expiration is optional and not claimed as verified. |

UI, availability, licensing, and preview status can vary by tenant and change over time. Use the dates, prerequisites, official references, and completion criteria in each guide; a connection badge or HTTP 200 alone is not an end-to-end success criterion.
