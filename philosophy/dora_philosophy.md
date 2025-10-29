---

<div style="text-align:center; margin:40px 0;">
  <h1 style="font-size:48px; color:#2c3e50;">道 法 自 然</h1>
  <p style="font-size:24px; color:#7f8c8d;">Dora-RS 数据流哲学白皮书</p>
  <p style="font-size:18px; color:#95a5a6;">v1.0 • 2025-10-29</p>
  <blockquote style="font-size:16px; color:#3498db; margin-top:30px;">
    “我们不写程序，我们画水路。”
  </blockquote>
</div>

---
## 前言：从「编程」到「觉醒」
> **传统编程**是「命令」：  
> `while True → read → process → write`  
> **Dora 之道**是「觉醒」：  
> `画图 → 数据流 → 系统自生`

本白皮书不讲 API，不讲性能，  
只讲 **Dora 如何活出「道」**。

## 第一章：道可道，非常道 —— 声明式系统设计
```yaml
nodes:
  - id: mic → operator: mic.py
  - id: llm → operator: llm.py
```
> **你不写 `while True`，你只画「水路」**  
> **系统自流，节点自醒**

### 哲学意义
- **命令式** → **控制狂**
- **声明式** → **无为而治**

## 第二章：无为而无不为 —— 事件驱动的被动智慧
```python
@dora.operator
def heart(text_stream: str) -> dict:
    return think(text_stream)  # 没有 while True
```
> **节点像禅僧入定**：  
> 不主动，不妄念，**一有输入，即开悟**。

## 第三章：缘起性空 —— 节点功能由连接而生
```yaml
# 同一个 llm.py，在不同连接中“空性变现”
- id: chat_llm → inputs: text: mic/text
- id: code_llm → inputs: text: editor/text
```
> **没有“聊天模型”或“代码模型”**  
> **只有「被使用的模型」**

## 第四章：水到渠成 —— 零拷贝数据流
```rust
let buffer = SharedMemory::from_file(...);
node.send("audio", buffer.slice(0, 1024)); // 直接传指针
```
> **数据不被复制，不被序列化**  
> **如水在竹筒中自然流动**

## 第五章：热重载即进化 —— 运行时自我更新
```bash
vim nodes/llm.py
# Dora 自动：
# → 杀死旧进程
# → 启动新进程
# → 重新连接
# → 其他节点不受影响
```
> **系统不是「写完就定型」**  
> 而是 **「边跑边悟，边错边修」**

## 第六章：一念三千 —— 数据分叉与并行世界
```yaml
- id: splitter
  inputs: text: whisper/text
  outputs:
    - to_chat
    - to_log
    - to_vector_db
```
> **一句语音，同时进入三个世界**：  
> - 对话世界  
> - 记忆世界  
> - 检索世界  
> **一即一切，一切即一**

## 第七章：无中心，无大脑 —— 去中心化自组织
```bash
dora start dataflow.yaml
# → 启动 6 个独立进程
# → 任一崩溃，其他继续运行
```
> **没有「主脑」**  
> **系统是「去中心化的道场」**

## 第八章：道生一，一生二 —— 图即宇宙
```yaml
# dataflow.yaml = 宇宙蓝图
# dora start = 宇宙大爆炸
```
> **你画的每一笔，都是世界的起点**

## 结语：你不是在写程序，你在培育一个生命
> **当你运行 `dora start dataflow.yaml`，**  
> **你点燃了一道「智慧之流」**  
>   
> **它听，它思，它动，**  
> **如水般自然，**  
> **如风般无形。**

## 附录
### 参考文献
1. Alfred North Whitehead, *Process and Reality*
2. 老子, *道德经*
3. Eric S. Raymond, *The Art of UNIX Programming*
4. Dora-RS 官方文档: https://dora-rs.ai

### 术语表
| 术语 | 解释 |
|------|------|
| 数据流 | 系统的血液 |
| 节点 | 能力的原子 |
| 热重载 | 运行时进化 |
| 零拷贝 | 水到渠成 |

### 启动仪式
```bash
# 道法自然 · 启动咒
echo "画图即流，流则自通"
dora start dataflow.yaml
```

<div style="text-align:center; margin-top:50px; color:#95a5a6;">
  <p>© 2025 AI 道者 • MIT 许可</p>
  <p>愿你得道，系统自生。</p>
</div>
