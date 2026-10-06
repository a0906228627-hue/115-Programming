# AGENTS.md

> Freshman programming coursework repo (`大一計算機程式`). Currently greenfield: only `README.md` + Python `.gitignore`, no source, manifests, tests, CI, or lint config yet.

## 語言與回應
- 一律使用繁體中文回應。
- 程式語言為 Python。

## Python / Conda（已驗證）
- 套件一律用 conda 管理，不用 pip / venv / poetry。
- 固定使用 `iem_python` 環境（Python 3.12.13）。
- conda 不在 PowerShell PATH 上，必須用完整路徑呼叫：
  `& "$env:USERPROFILE\anaconda3\Scripts\conda.exe" run -n iem_python python <script.py>`
- 安裝套件：`& "$env:USERPROFILE\anaconda3\Scripts\conda.exe" install -n iem_python <pkg>`

## Working conventions
- Shell is Windows PowerShell 5.1. Use `workdir` param instead of `cd`; chain with `; if ($?) { ... }`.
- Use dedicated file tools (`read`/`edit`/`write`, `glob`/`grep`) over shell file ops.
- Prefer adding minimal standard Python tooling only when asked: `pytest`, `ruff`, or `mypy` — don't scaffold unprompted.
- Keep solutions simple and self-contained; this is coursework, not a service.
- Commit/push/PR only when explicitly requested.
