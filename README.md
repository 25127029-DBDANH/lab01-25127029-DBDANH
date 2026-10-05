# Lab 01 – Study Assistant (starter)

Trợ lý hỏi đáp rule-based đơn giản: cho biết phòng và giờ làm việc của các văn phòng trong trường.

## Prerequisites
- Python 3.10+
- Git

## Setup
```bash
git clone git@github.com:25127029-DBDANH/lab01-25127029-DBDANH.git
cd lab01-25127029-DBDANH
python -m venv .venv
source .venv/bin/activate        # Windows Git Bash: source .venv/Scripts/activate
                                 # Windows PowerShell: .venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
pip install -e .
```

## Run
```bash
python -m assistant "where is the IT helpdesk?"
```

## Test
```bash
pytest -q
# -> 4 passed
```

## Project structure
- `src/assistant/` – mã nguồn
- `tests/` – test tự động
- `data/` – dữ liệu mẫu
- `docs/` – tài liệu
- `ui/` – giao diện
- `scripts/` – script hỗ trợ

## Troubleshooting
- `No module named assistant` → chưa activate `.venv` hoặc quên `pip install -e .` (nhớ có dấu chấm)
- `python: command not found` (Windows) → dùng `py -m venv .venv` để tạo venv
- PowerShell chặn `Activate.ps1` → `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`