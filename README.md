# dungpp-assistant

Bộ trợ lý cá nhân cho **Phạm Phú Dũng** — Android Developer @ iKame Global.

Plugin này gói 4 skill mà Claude sẽ tự động kích hoạt theo ngữ cảnh:

| Skill | Mô đích | Kích hoạt khi... |
|-------|---------|------------------|
| `brand-voice` | Viết nội dung theo phong cách iKame | "viết email", "soạn thông báo", "viết kiểu iKamer" |
| `company-knowledge` | Hỏi đáp về iKame (vision, mission, values) | "iKame là gì", "giá trị công ty", "giới thiệu iKame" |
| `personal-profile` | Áp dụng working rules của Dũng | Mặc định trong session kỹ thuật, "review code", "lên plan" |
| `work-templates` | Báo cáo tuần, IDP, learning plan, Medium curation | "báo cáo tuần", "làm IDP", "tìm bài Medium" |

## Cài đặt

Trong Claude Cowork, kéo file `dungpp-assistant.plugin` vào chat và bấm Install.

## Cấu trúc

```
dungpp-assistant/
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   ├── brand-voice/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── core-values.md
│   │       └── examples.md
│   ├── company-knowledge/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── company-profile.md
│   ├── personal-profile/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── about-dung.md
│   └── work-templates/
│       ├── SKILL.md
│       └── references/
│           ├── weekly-report-template.md
│           ├── idp-template.md
│           ├── learning-plan-template.md
│           └── medium-curation.md
└── README.md
```

## Cập nhật

Khi muốn bổ sung file (ví dụ: brand guideline chính thức, IDP mới, template mới), chỉnh trong thư mục `references/` của skill tương ứng rồi đóng gói lại:

```bash
cd dungpp-assistant
zip -r ../dungpp-assistant.plugin . -x "*.DS_Store"
```

## Version

0.8.0 — bổ sung `performance-checkpoint-guide.md` với cẩm nang Performance Checkpoint chính thức của iKame từ iWiki. 5 mức rating, công thức iKameWHAT 70% + iKameHOW 30%, hướng dẫn Tự đánh giá/Feedback360/1:1. Section "Áp dụng cho Mid-year Checkpoint 6/2026" map evidence Dũng đã có với từng phần checkpoint.

0.7.2 — bổ sung báo cáo tuần W3/5 + Manager feedback 4⭐ "Làm xuất sắc". Update evidence mapping cho Tech R&D #15 (security incident response).

0.7.1 — bổ sung báo cáo tuần W4/2, W1/3, W3/3 từ user share + insight về Manager request "UT trong IDP" + Tech R&D 4.3.

0.7.0 — bổ sung `weekly-reports-h1-2026.md` tổng hợp 8 báo cáo tuần đã fetch từ iGoal: AI Home → AI Chat IAP, manager ratings 4⭐-5⭐, evidence mapping cho 17 gap behaviors. Plugin giờ có track record thật của Dũng để Claude reference.

0.6.0 — thay weekly-report-template.md bằng **OFFICIAL iKame template** với 6 sections (IKAME WHAT/HOW/LEVEL UP/Tồn đọng/Hỗ trợ/Tự đánh giá). Mỗi section có guidance chi tiết và rule tự động tag với EKS + 17 gap behaviors.

0.5.0 — bổ sung `eks-h1-2026.md` với EKS H1 2026 của Dũng @ Android BU3, mapping từng KS vào competency framework và 17 gap behaviors. Cập nhật about-dung.md với job level + team info.

0.4.0 — bổ sung `assessment-result.md` với kết quả self-assessment iGrow 1/2026 (Middle 2 → Senior 1), gap map chính xác 17 hành vi = IDP draft của Dũng. Plugin giờ có ground truth để Claude align mọi đề xuất với gap thực tế.

0.3.0 — bổ sung TOÀN BỘ khung năng lực iKame từ iGrow (8 năng lực / 26 sub-skills / 6 levels) vào `competency-framework.md`, kèm `senior-promotion-playbook.md` với gap analysis + action plan 4 quý + evidence checklist.

0.2.0 — bổ sung Senior Mobile Developer framework 2026 (4 nhóm năng lực iKame: Innovation / Continuous Development / Ownership / Android Tech R&D) vào personal-profile và work-templates.

0.1.0 — khởi tạo với 4 skill cơ bản dựa trên iKame core values và profile cá nhân.

## Mục tiêu năm 2026 của Dũng

🎯 **Lên Senior Mobile Developer** — plugin này được build để Claude luôn align mọi đề xuất với mục tiêu đó.

## Roadmap mở rộng

- [ ] Thêm reference cho từng product team Dũng đang work (AI Home / AI Learn / AI Chat)
- [ ] Skill mới: Figma MCP workflow (design-to-code)
- [ ] Skill mới: Code review checklist cho Android (gắn với KPI mentor Hiếu < 30p)
- [ ] Skill mới: Security baseline checklist (R8 + Play Integrity)
