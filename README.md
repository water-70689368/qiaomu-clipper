# qiaomu-clipper PR evidence

These screenshots contain only the excerpts authorized by the reporter for the upstream bug report. Browser chrome, account sidebar, conversation identifiers and unrelated content are excluded. Cropping and comparison labels are the only image processing; article pixels are not redrawn.

## Code preservation

Each comparison reads left to right: original ChatGPT page, installed stock Qiaomu 1.18.4, test build based on upstream 1.18.7 (2cabb0184276b8fdb288b38f93f0d239e8ecaf40) with the code preservation patch. Captured in the same AdsPower Chromium 147 environment. The existing dark and light reader themes were retained. Font size and syntax colors differ; the claim is preservation of line breaks, blank lines, indentation and diagram structure, not pixel-identical styling. Regression tests also reproduce the loss with upstream Defuddle 0.19.2 independently of the version difference.

- latency: section “4. 为什么实际用 Pipecat 时通常延迟比较低？”
- python: indented Pipeline constructor
- pipeline: multiline microphone/STT/LLM flow

Source hash of the tested fix: 95c89379e972d94e433a8a178fb7fa7070727827c3ac4b86c584455b0139fffa.

## Original-page AI conversation

ai-chat-original-page-prototype.png is an actual Chrome screenshot of the earlier 1.18.4-based implementation, using an authored public local fixture and a deterministic local mock model. It demonstrates original-page + native side panel layout and correct page-B context. It is not a screenshot of the final rebased PR build, nor an external-model quality evaluation. The later PR is based on 1.18.7 and has independent automated validation. The public HTML fixture can be served locally for a fresh manual run.
