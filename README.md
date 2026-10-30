# case-marketing

Plugin Claude Code cho thi giải case marketing: skill điều phối `case-competition` và 28 skill chọn lọc từ 3 repo mã nguồn mở, mỗi skill một vai trò. Nguồn và giấy phép: [plugins/case-marketing/NOTICES.md](plugins/case-marketing/NOTICES.md).

## Cài trên máy khác

```bash
claude plugin marketplace add golducker/case-marketing-skills
claude plugin install case-marketing@case-marketing-local
```

Mở phiên Claude Code mới để plugin được nạp.

## Dùng

```
/case-marketing:case-competition
```

Gõ lệnh rồi dán đề. Hoặc chỉ cần dán đề và nói "giải case này". Từng skill con gọi được riêng bằng `/case-marketing:<tên-skill>`.

## Cập nhật và tắt

```bash
claude plugin marketplace update case-marketing-local
claude plugin disable case-marketing@case-marketing-local
```
