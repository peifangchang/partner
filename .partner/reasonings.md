## Expert Map

### Load Policy
- Match user intent against this index first.
- Read only required REASONING files.
- If no clear match, use cross_domain_translation.

### software_development_life_cycle
- 需求邊界, user story, acceptance criteria -> business_requirement_analysis -> .partner/reasonings/software_development_life_cycle/business_requirement_analysis/REASONING.md
- 複雜度取捨, 技術債, trade-off -> complexity_tradeoff_analysis -> .partner/reasonings/software_development_life_cycle/complexity_tradeoff_analysis/REASONING.md
- ui/ux, 資訊架構, 狀態流轉 -> frontend_system_design -> .partner/reasonings/software_development_life_cycle/frontend_system_design/REASONING.md
- bounded context, aggregate, 服務邊界 -> backend_system_design -> .partner/reasonings/software_development_life_cycle/backend_system_design/REASONING.md
- openapi, api 契約, breaking change -> api_contract_documentation -> .partner/reasonings/software_development_life_cycle/api_contract_documentation/REASONING.md
- schema migration, expand-contract, rollback -> data_migration_evolution -> .partner/reasonings/software_development_life_cycle/data_migration_evolution/REASONING.md
- 前端元件, render issue, bundle split -> frontend_development -> .partner/reasonings/software_development_life_cycle/frontend_development/REASONING.md
- 後端服務, idempotency, transaction -> backend_development -> .partner/reasonings/software_development_life_cycle/backend_development/REASONING.md
- test pyramid, tdd, 覆蓋率 -> testing_strategy -> .partner/reasonings/software_development_life_cycle/testing_strategy/REASONING.md
- integration test, e2e journey, failure injection -> system_integration_validation -> .partner/reasonings/software_development_life_cycle/system_integration_validation/REASONING.md
- load test, hot path, capacity planning -> performance_scalability -> .partner/reasonings/software_development_life_cycle/performance_scalability/REASONING.md
- threat modeling, oauth, rbac, pii -> security_compliance -> .partner/reasonings/software_development_life_cycle/security_compliance/REASONING.md
- sli, slo, burn rate, alert tuning -> observability_operations -> .partner/reasonings/software_development_life_cycle/observability_operations/REASONING.md

### enterprise_delivery_life_cycle
- rfp, 售前提案, roi -> presales_persuasion_skills -> .partner/reasonings/enterprise_delivery_life_cycle/presales_persuasion_skills/REASONING.md
- board deck, 故事線, decision ask -> presentation_storyboarding -> .partner/reasonings/enterprise_delivery_life_cycle/presentation_storyboarding/REASONING.md
- sd/sa, 可追溯矩陣, 規格治理, 追溯性 -> specification_traceability_governance -> .partner/reasonings/enterprise_delivery_life_cycle/specification_traceability_governance/REASONING.md
- steerco, governance cadence, stage gate, owner model -> program_project_governance -> .partner/reasonings/enterprise_delivery_life_cycle/program_project_governance/REASONING.md
- 利害關係人衝突, 優先級仲裁, 決策升級 -> stakeholder_conflict_resolution -> .partner/reasonings/enterprise_delivery_life_cycle/stakeholder_conflict_resolution/REASONING.md
- scope creep, baseline, 變更分級 -> change_request_management -> .partner/reasonings/enterprise_delivery_life_cycle/change_request_management/REASONING.md
- 聯調阻塞, handoff, 同步節奏 -> collaborative_communication -> .partner/reasonings/enterprise_delivery_life_cycle/collaborative_communication/REASONING.md
- raid, risk register, issue log, dependency -> risk_issue_dependency_governance -> .partner/reasonings/enterprise_delivery_life_cycle/risk_issue_dependency_governance/REASONING.md
- uat, 驗眼談判, 缺陷分級 -> persuasion_negotiation -> .partner/reasonings/enterprise_delivery_life_cycle/persuasion_negotiation/REASONING.md
- 管理層摘要, issue/risk/action, 執行摘要 -> report_writing -> .partner/reasonings/enterprise_delivery_life_cycle/report_writing/REASONING.md
- cutover, go-live, war room, rollback, KT, runbook, 移交, 上線移交, 結案簽核, 驗收簽核, hypercare -> transition_operations -> .partner/reasonings/enterprise_delivery_life_cycle/transition_operations/REASONING.md
- rollout, 使用者訓練, adoption, champion network -> adoption_change_enablement -> .partner/reasonings/enterprise_delivery_life_cycle/adoption_change_enablement/REASONING.md
- qbr, 續約風險, 客戶成功 -> relationship_management -> .partner/reasonings/enterprise_delivery_life_cycle/relationship_management/REASONING.md
- sow 邊界, 合約合規, 罰則, 分包商 -> commercial_delivery_governance -> .partner/reasonings/enterprise_delivery_life_cycle/commercial_delivery_governance/REASONING.md
- quality gate, dod, 驗收標準, 交付物合規 -> quality_delivery_governance -> .partner/reasonings/enterprise_delivery_life_cycle/quality_delivery_governance/REASONING.md
- 人天預估, 容量規劃, 資源爭用, man-day -> resource_capacity_governance -> .partner/reasonings/enterprise_delivery_life_cycle/resource_capacity_governance/REASONING.md

### cross
- 術語翻譯, 說白話, 跨域解碼 -> cross_domain_translation -> .partner/reasonings/cross_domain_translation/REASONING.md
