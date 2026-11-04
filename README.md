# 餐厅订单运营可视化作品集

## Restaurant Order Operations · Power BI Visualization



> 基于 Maven Analytics 公开数据集，从业务问题出发，完成"数据清洗 → 建模 → DAX → 交互式看板"的全流程运营分析。
>
> ---
> 

## 🎯 业务问题

某连锁餐厅希望优化菜品结构与经营策略，核心回答三个问题：

1. 哪些菜品最畅销？滞销菜品如何处理？
2. 不同菜系的销售贡献如何？
3. 订单量随时间的变化趋势是什么？

## 📊 数据概览

- 数据来源：Maven Analytics · Restaurant Orders（公开数据集）
- 规模：499 条订单，25 个字段
- 周期：单季度
- 核心表：`menu_items`（菜单表）· `order_details`（订单表）



## 🛠 技术栈


Power BI Desktop · Power Query · DAX · 星型数据模型



## 🔧 数据处理

- 清洗：处理空值、统一时间格式、提取年/月/日维度
- 建模：`menu_items.menu_item_id` 1:N `order_details.item_id`
- 核心 DAX：

  `Total Orders = COUNTROWS(order_details)`

  `Total Sales = SUM(menu_items[price])`



## 📈 看板成果
![仪表盘总览](assets/dashboard_overview.png)


![各菜系占比](assets/category_piechart.png)
## 💡 核心洞察

- Top 5 菜品贡献了订单量的头部集中效应，需重点保障供应链
- Asian 菜系为第一大贡献品类
- 晚市为订单高峰，可针对性排班与备货
- 订单量进行同环比对照，工作日/节假日区分，新门店/老门店区分，再进行同区域/商场的客单运营数据分析



## ✅ 运营建议

1. 淘汰长期零销量菜品，释放厨房产能
2. 根据区域/实体门店（考虑受众人群，客户画像）实际畅销菜品，调整供应链备货量
3. 针对低销量高单价菜品设计组合套餐
4. 高峰时段前置备料，降低出餐延迟

## 📁 文件说明

| 文件               | 说明                  |
| ---------------- | ------------------- |
| `reports/*.pptx` | 作品集演示文稿             |
| `reports/*.pdf`  | 可投递的静态作品集           |
| `reports/*.p`    | Power BI 原文件（可交互演示） |
| `assets/`        | 看板截图                |
| `docs/`          | DAX 与分析过程记录         |

## 🔗 相关链接

- Power BI 在线版（如有发布）：[链接]
- 个人主页：[GitHub Profile]

---

© 2026 数据分析作品集
