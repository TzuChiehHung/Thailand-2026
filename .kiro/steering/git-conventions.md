---
inclusion: always
---

# Git 版本控制準則

本文件規範本專案的 git 操作與 commit 訊息格式，適用於所有版本控制情境。

## 操作安全規範（嚴格遵守）

- **嚴禁自動 push**：任何情況下都不得主動執行 `git push`。唯有使用者在當次對話中明確要求「push」時，才可推送。
- **Commit 前需先確認**：執行 `git commit` 之前，必須先將擬定的 commit message 列給使用者過目，待使用者確認後才可提交。
- 除非使用者明確要求，否則不得使用破壞性指令（`push --force`、`reset --hard`、`clean -f`、`branch -D` 等）。
- 不得修改 git config。
- 暫存檔案時優先逐一指定檔名，避免 `git add -A` / `git add .` 夾帶非預期變更。

## Commit 訊息格式

- 採用 **Conventional Commits** 格式，語言使用**英文**。
- 格式：`<type>(<scope>): <description>`
- 常用 type：`feat`、`fix`、`docs`、`style`、`refactor`、`chore`。
- scope 建議以頁面或天數標示，例如 `docs(day1)`、`feat(costs)`、`chore(kiro)`。
- description 簡潔扼要，說明變更重點。

## 排除項目

- 暫存／轉檔用的臨時檔案（如 `temp.html`、轉檔產生的圖片）不得納入版本控制。

---

*本準則由 senior 規劃師（Antigravity）維護，請嚴格遵守以確保版本控制流程一致。*
