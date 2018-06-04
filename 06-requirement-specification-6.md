---
layout: default
title: Supplementary Requirements
---
# Owl 需求规格说明

## 6.6 Supplementary Requirements

### 补充性规格说明

#### 修订历史
| 版本 | 日期 | 描述 | 作者 |
| :--: | :--: | :--: | :--: |
| 初始草案 | 2018-06-03 | 第一个草案。主要在细化阶段中进行精化。 | Summer |

#### 简介
本文档记录了Owl Movies里所有没有在用例描述中描述的需求。

#### 功能性
1. 日志和错误处理
在持久性存储中记录所有错误。
2. 同步处理
在不同的设备上对同一个账号的操作具有同步性。

#### 可用性
人性因素
- 在展示页面尽量使用宣传海报+少量文字，让用户能够直观对电影有感觉。
显示因素
- 要设计成响应式布局，根据窗口大小调整布局，避免出现某些信息被隐藏的情况。

响应要快速流畅，避免使用不流畅而给用户带来不好的体验。

#### 可靠性
1. 可恢复性
使用支付授权服务时出现错误，需要尝试使用本地解决方案如储存和转发。
2. 性能
能够容纳多人同时使用而不奔溃，需要考虑高性能高并发的问题。

#### 可支持性
1. 多平台支持
该网站应该能够在PC端和客户端都正常显示，除此以外，在不同的浏览器上也应该保证显示一致，所以应该对主流浏览器做一些单独的特殊处理。

#### 实现约束
该网站坚持采用Vue.js作为前端框架并且采用python作为后端开发语言。

#### 接口
该网站只需要软件接口。
- 第三方授权支付的接口
- 与电影院信息同步的接口
- 短信验证码服务接口

#### 应用领域(业务)规则
| ID | 规则 | 可变性 | 来源 |
| :--: | :--: | :--: | :--: |
| 规则1 | 预定电影票并且支付成功之后，不可以更换电影、电影场次以及电影座位 | 低 | 电影院规则 |
| 规则2 | 购买电影票后无法退票 | 中 在线售票平台可以提供转让票或其他类似功能让用户享有类似退票的体验 | 电影院规则 |
| 规则3 | 每周有购票优惠并且每个账号限购两张 | 高 优惠政协随时可能改变 |  |

#### 法律问题
我们需要使用一些开源构件，因此我们要注意其许可限制问题，要注意包含该开源构件的产品是否能用于商业用途。并且在交易过程中，我们需要注意税务问题。
