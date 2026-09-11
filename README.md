# Copilot Studio Hands-on Labs

[English](README.md) | [한국어](README.ko.md)

Build a Copilot Studio agent, configure its knowledge and tools, and confirm its behavior using the same assets. This repository contains two self-contained guides in English and Korean, plus eight recorded walkthroughs: **Create** and **Use** for each guide in both languages.

**English is the default documentation language.** Korean editions are also included.

📖 **Read the guides online — no download required:** <https://junwoojeong100.github.io/microsoft-copilot-studio-labs/>

## Choose a guide

| Guide | Intended audience and outcome | English | Korean |
|---|---|---|---|
| Beginner | Business users and first-time makers: a synthetic HR FAQ agent, grounded answers, leave-request input validation, and personal Teams use | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.html) | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.ko.html) |
| Azure developer | Developers: REST APIs, Foundry models, MCP, Foundry IQ retrieval, and approval workflows with explicit authentication and execution evidence | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.html) | [Open guide](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.ko.html) |

**Before you start:** Check the minimum participant account and permissions — [Beginner](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-hands-on-lab.html#minimum-access) · [Azure developer](https://junwoojeong100.github.io/microsoft-copilot-studio-labs/copilot-studio-lab-for-azure-devs.html#minimum-access). Each checklist includes where to verify access, when to stop, and a separate expandable administrator-preparation section.

The beginner core path is **L01 → L02 → L03 → L09**. For the developer guide, complete **Lab 0: base-agent preparation** before the five core labs **L04 → L05 → L12 → L14 → L20**. Lab 0 is a preparatory step, not an additional core completion item. **L08 Foundry Agent** is an additional optional/preview lab included in the developer recordings.

The developer guide assumes familiarity with the beginner concepts but includes its own minimal agent setup. Completing the beginner guide does not imply completion of the developer guide. A detailed comparison is available in each guide's reference appendix.

## Recorded walkthroughs

| Guide | Create | Use |
|---|---|---|
| Beginner · English | [4 min 30 sec](copilot-studio-hands-on-lab-create-en-20260910.mp4) | [3 min 17 sec](copilot-studio-hands-on-lab-use-en-20260910.mp4) |
| Azure developer · English | [10 min 34 sec](copilot-studio-lab-for-azure-devs-create-en-20260910.mp4) | [8 min 25 sec](copilot-studio-lab-for-azure-devs-use-en-20260910.mp4) |

The English guides link to these **English-captioned recordings with actual English lab requests**. The [original four Korean recordings](README.ko.md#실습-녹화-영상) remain unchanged. The developer videos include GHC's Learn MCP, IQ retrieval, and expense-intake workflows, but not every optional GHC reference lab.

**Recorded fallback:** Fresh Standard API-agent initialization did not complete, so the English developer walkthrough explicitly uses a prepared English Standard draft. New GHC agents, tools, lists, and workflow copies are used. Shared Foundry/IQ sources may retain Korean provenance markers or document titles; these are actual source data, not translated screenshots.

The HTML guides include chapter timestamps. Video duration is not the time required to perform the labs; approval, provisioning, indexing, and publication delays are separate.

All eight MP4s are below GitHub's normal Git limit of **100 MiB per file**; that limit is not a combined-size limit. Keep the original video quality and push with Git rather than relying on the browser upload's smaller limit. See [GitHub's file-size guidance](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github).

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

Use the executable snippets and sample values from the edition you are following: the English guides use English instructions, inputs, and expected values, while the Korean guides use Korean examples. Do not mix language-specific topic names, input names, status values, or comparison strings between editions. Keep reserved API identifiers as written, and replace placeholders such as `<LAB_PREFIX>` using each guide's naming rules.

The language switch in each guide opens the corresponding language edition. Progress checkboxes are a local convenience, not evidence that a cloud operation succeeded.

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
