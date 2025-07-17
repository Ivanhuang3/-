
<img width="1122" height="635" alt="架構圖(浮水印)" src="https://github.com/user-attachments/assets/f06f1bcd-4e27-4639-b45d-e83e22f43b07" />


# ☁️ 經典雲端高併發架構

本專案展示一套基於 AWS 原生服務的**高可擴展、前後端分離且具備高可用性**的雲端架構設計。此架構支援高併發工作負載，自動擴展、跨可用區容錯與即時監控，適合現代企業應用。

---

## 📌 架構圖

> 此架構設計特色：
> - 前端透過 **CloudFront + WAF + Route 53 + ACM** 進行全球加速與 DNS 管理  
> - 公有子網內的 EC2 透過 **Elastic Load Balancer (ALB/NLB)** 處理外部請求  
> - 私有子網內的後端服務處理內部邏輯並連接資料庫與快取服務  
> - 使用 **NAT Gateway** 提供私有子網安全連外通道  
> - 資料層使用 **RDS 與 ElastiCache**，支援跨可用區備援  
> - 透過 **CloudWatch、Grafana、CloudTrail** 進行即時監控與稽核追蹤  


---

## 🔧 核心組件

| 類別             | 使用的 AWS 服務                                                                 |
|------------------|----------------------------------------------------------------------------------|
| 前端與路由       | CloudFront、WAF、Route 53、ACM                                                  |
| 網路與通訊       | Internet Gateway、NAT Gateway、VPC、子網                                        |
| 運算層（後端）   | Amazon EC2、Auto Scaling Group、AMI                                             |
| 負載平衡         | ALB（應用層）、NLB（傳輸層）                                                    |
| 資料儲存         | Amazon RDS（多可用區）、Amazon ElastiCache                                     |
| 靜態儲存         | Amazon S3                                                                        |
| 監控與稽核       | CloudWatch、Grafana、AWS CloudTrail                                              |

---

## 🌟 架構亮點

- ⚙️ EC2 後端支援 Auto Scaling 自動擴展與故障容錯  
- 🔄 RDS 支援多可用區備援部署，確保資料高可用  
- 🌐 前後端分離設計，S3 + CloudFront 提供靜態內容全球加速  
- 🔒 WAF 與 ACM 提供 HTTPS 與應用層安全防護  
- 📊 CloudWatch、Grafana、CloudTrail 提供完整即時監控與稽核追蹤

---

