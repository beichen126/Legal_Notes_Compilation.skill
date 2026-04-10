# 法学笔记整理 Skill V0（定稿版）

**文档位置**：`/root/.openclaw/workspace/法学笔记整理_skill_v0.md`

## 概述

本skill用于将法学教材整理为高质量Markdown笔记并转换为PDF。

**核心目标**：在"内容压缩"与"信息丰富"之间取平衡，做出"有密度但不过度"的笔记。

---

## 核心理念

### 1. 无损压缩理念

**定义**：笔记整理不是简单的删减，而是在保留所有关键信息的前提下进行压缩。

**原则**：
- **禁止**：教材讲好几页的内容，笔记几行略过
- **要求**：读者读笔记的理解程度 ≈ 读教材的理解程度
- **方法**：
  - 用表格压缩对比性内容（如学说对比）
  - 用列表压缩并列性内容
  - 用结构化语言压缩叙述性内容

### 2. 信息可视化理念

**定义**：能用表格、图表呈现的内容，不用纯文字叙述。

**必须使用表格的场景**：
- 学说对比（人物、核心主张、评价）
- 分类列举（三要素、三原则、三阶段）
- 时间线/发展历程
- 法条对比（新旧法对比）

### 3. 信息密度最大化

**目标**：每一行文字都应承载有效信息。

**方法**：
- 删除过渡性、铺垫性语句
- 删除重复性表述
- 删除与核心知识无关的背景信息
- 合并相似要点
- 使用精准、凝练的法律术语

### 4. 避免重复性表述

**处理原则**：
- 概念首次出现时完整定义
- 后续提及用简称或指代
- 同一要点不在多处重复展开
- 案例说理与概念说明不重复

### 5. 禁止篡改、编造内容

**红线**：不得杜撰、虚构、编造。

**法条要求**：
- 必须来自教材原文或权威法律数据库
- 必须保留准确的条文编号
- 必要时可联网搜索核实

**案例要求**：
- 必须来自教材原文或权威判例
- 必须保留案名、关键事实、判决要旨
- 不得自行编造案例名称或案情

---

## 一、格式标准（强制性）

### 1.1 标题层级体系

**⚠️ 绝对禁止：以"章"作为一级标题**

#### ✅ 正确格式：

```markdown
# 第一节 节标题

**本节评估**：教材约X页，知识点密度[高/中/低]，考试重要度[高/中/低] → **[A/B/C级]**（目标篇幅：XXX-XXX行）

---

## 一、一级标题

### （一）二级标题

#### 1. 三级标题（极少使用）

**核心概念**：具体内容

**重要说明**：补充解释
```

#### ❌ 绝对禁止：
```markdown
# 第四章 章标题          ← 禁止！
## 第一节 节标题         ← 禁止！一级必须是#
```

#### 层级对应关系：
- 一级：`# 第一节 节标题`
- 二级：`## 一、标题内容`
- 三级：`### （一）标题内容`
- 四级：`#### 1. 标题内容`（极少用）

### 1.2 固定模块标签

| 标签 | 使用场景 | 示例 |
|:-----|:---------|:-----|
| **核心概念** | 概念定义 | 涉外 = 涉及外国因素 |
| **重要说明** | 关键限定 | 上述三要素只要其一涉外即可 |
| **立法进步** | 法律演变评价 | 新增"经常居所地"标准 |
| **学术争议** | 不同学说观点 | 肯定说 vs 反对说 |
| **历史意义** | 历史地位评价 | 被誉为"近代国际私法之父" |
| **理论缺陷** | 学说局限性 | 循环论证问题 |
| **方法论贡献** | 方法论创新 | 采用实证方法 |

### 1.3 表格格式

```markdown
| 列1 | 列2 | 列3 |
|:-----|:-----|:-----|
| 内容 | 内容 | 内容 |
```

### 1.4 强调与引用

| 格式 | 使用场景 | 示例 |
|:-----|:---------|:-----|
| `**加粗**` | 核心概念、关键术语 | **法律关系本座说** |
| `> 引用块` | 法条原文、经典表述 | > "诸化外人，同类自相犯者，各依本俗法" |
| `---` | 分隔大段内容 | --- |

### 1.5 英文翻译保留规则

| 类型 | 处理方式 | 示例 |
|:-----|:---------|:-----|
| 概念术语 | 括号内保留 | 万民法(jus gentium) |
| 学说名称 | 括号内保留 | 法则区别说(statuta theory) |
| 人名 | 括号内保留拼写 | 萨维尼(Savigny) |
| 法学术语 | 括号内保留拉丁文 | 场所支配行为(locus regit actum) |
| 普通名词 | 可省略 | "方法"、"原则"等 |

---

## 二、内容评估与篇幅分配

### 2.1 章节等级划分

| 等级 | 评分范围 | 笔记篇幅 | 策略 |
|:-----|:-----|:---------|:-----|
| **A级** | 80-100 | 教材×80-120% | 详细展开 |
| **B级** | 50-79 | 教材×50-80% | 平衡处理 |
| **C级** | 0-49 | 教材×30-50% | 高度概括 |

### 2.2 压缩率计算公式

**节级压缩率**：
```
压缩率 = (raw文件字符数 - md文件字符数) / raw文件字符数 × 100%
```

**章级压缩率**：
```
压缩率 = (原PDF页数 - 笔记PDF页数) / 原PDF页数 × 100%
```

**字符统计**：去除空格和换行后的纯文本字符

### 2.3 强制压缩率标准

| 压缩率 | 状态 | 处理 |
|:------:|:----:|:----:|
| <35% | 偏低 | ✅ 可接受，内容较详细 |
| 35-65% | 正常 | ✅ **理想范围** |
| 65-75% | 偏高 | ⚠️ 需检查，可能存在过度压缩 |
| >75% | 禁止 | ❌ **必须重做** |

**绝对禁止**：压缩率>75%的章节直接提交

---

## 三、详略取舍标准

### 3.1 必须详细保留（压缩率<30%）

| 内容类型 | 保留要求 |
|:---------|:---------|
| 核心概念定义 | 完整保留，准确表述 |
| 学说核心主张 | 保留完整论点、代表人物、标志性表述 |
| 法典条文原文 | 引用块完整引用，保留条文编号 |
| 典型案例 | 保留案名、核心事实、判决要旨 |
| 学说对比 | 以表格形式保留各家观点差异 |
| 学者评价 | 保留权威性评价 |

### 3.2 适当压缩（30-55%）

| 内容类型 | 处理方式 |
|:---------|:---------|
| 历史背景 | 概括关键转折点和因果关系 |
| 论证过程 | 压缩为逻辑链条或要点 |
| 脚注引用 | 保留核心文献，一般性引用可省略 |
| 案例细节 | 保留关键要素，省略过程性描述 |
| 重复性表述 | 合并或省略 |

### 3.3 可大幅压缩或省略（>55%）

| 内容类型 | 处理方式 |
|:---------|:---------|
| 冗长的历史叙述 | 时间线或一句话概括 |
| 过细的脚注 | 仅保留页码和核心观点 |
| 重复举例 | 首次完整，后续提及即可 |
| 过渡性语句 | 删除 |
| 教材中的自谦/客套表述 | 删除 |

---

## 四、文件路径与命名规范

### 4.1 目录结构规范

```
workspace/
├── XX法笔记/                          # 课程总文件夹
│   ├── 第01章/                        # 章文件夹（两位数编号）
│   │   ├── sections/                  # 小节文件存放
│   │   │   ├── all_pages.txt          # 整章原始文本（必须保留）
│   │   │   ├── section1_raw.txt       # 第一节原始文本
│   │   │   ├── section1.md            # 第一节整理后
│   │   │   ├── section2_raw.txt       # 第二节原始文本
│   │   │   ├── section2.md            # 第二节整理后
│   │   │   ├── ...                    # 其他小节
│   │   │   └── XX法_第01章_完整笔记.md  # 合并后的完整笔记
│   │   ├── output/                    # 输出文件夹
│   │   │   ├── XX法_第01章_完整笔记.html
│   │   │   └── XX法_第01章_完整笔记.pdf
│   │   └── md_to_html_v2.py           # HTML转换脚本（需修改路径）
│   ├── 第02章/
│   └── ...
├── XX法_分章/                         # 分章PDF源文件夹
│   ├── 第01章_XXXXX.pdf
│   ├── 第02章_XXXXX.pdf
│   └── ...
├── 回收站/                            # 重新整理时备份旧文件
└── scripts/                           # 公共脚本文件夹
    ├── md_to_html_v2.py
    ├── pdf_to_text.py
    ├── extract_pages.py
    ├── merge_sections.py
    ├── compression_stats.py
    └── README.md
```

### 4.2 文件命名规范

| 文件类型 | 命名格式 | 示例 |
|:---------|:---------|:-----|
| 章文件夹 | `第XX章/` | `第01章/`、`第12章/` |
| 原始txt | `all_pages.txt` | `all_pages.txt` |
| 小节raw | `section[N]_raw.txt` | `section1_raw.txt` |
| 小节md | `section[N].md` | `section1.md` |
| A级小节细分 | `section[N]_[数字].md` | `section1_1.md` |
| 完整笔记 | `XX法_第XX章_完整笔记.md` | `国际私法_第01章_完整笔记.md` |
| HTML输出 | `XX法_第XX章_完整笔记.html` | - |
| PDF输出 | `XX法_第XX章_完整笔记.pdf` | - |
| 分章PDF | `第XX章_XXXXX.pdf` | `第01章_绪论.pdf` |

### 4.3 脚本路径规范

- **md_to_html_v2.py**：复制到各章目录，修改配置区的 `COURSE_NAME` 和 `CHAPTER_NUM`
- **公共脚本**：`/root/.openclaw/workspace/scripts/`

---

## 五、主进程与子代理工作流程

### 5.1 主进程前置检查

```python
# 主进程启动时执行：

def pre_check(course_name):
    """
    course_name: 如 "国际私法"、"国际经济法"
    """
    
    # 1. 检查分章PDF文件夹
    split_pdf_dir = f"/root/.openclaw/workspace/{course_name}_分章"
    if not os.path.exists(split_pdf_dir):
        raise Error(f"错误：{split_pdf_dir} 不存在，请先拆分PDF")
    
    pdf_files = [f for f in os.listdir(split_pdf_dir) if f.endswith('.pdf')]
    if len(pdf_files) == 0:
        raise Error(f"错误：{split_pdf_dir} 下没有PDF文件")
    
    # 2. 检查/创建工作环境
    notes_dir = f"/root/.openclaw/workspace/{course_name}笔记"
    os.makedirs(notes_dir, exist_ok=True)
    
    for i in range(1, 18):
        chapter_dir = f"{notes_dir}/第{i:02d}章"
        os.makedirs(f"{chapter_dir}/sections", exist_ok=True)
        os.makedirs(f"{chapter_dir}/output", exist_ok=True)
    
    # 3. 创建回收站
    os.makedirs("/root/.openclaw/workspace/回收站", exist_ok=True)
    
    return True
```

### 5.2 子代理任务类型

| 类型 | 场景 | 删除旧文件 | 备份要求 |
|:-----|:-----|:----------:|:--------:|
| **整理子代理** | 首次整理某章 | ❌ 否 | 无需备份 |
| **重新整理子代理** | 用户明确要求重做、压缩率>75% | ✅ 是 | **必须备份到回收站** |

### 5.3 子代理Skill注入

**所有子代理任务启动时必须注入以下内容**：

```python
skill_content = """
【必须遵守的规则】

1. 格式标准（第1章）
   - 一级标题必须是"节"，禁止用"章"
   - 二级标题用"一、"，三级用"（一）"
   - 学说对比必须用表格
   - 法条原文必须用引用块

2. 压缩率标准（第2.3节）
   - 理想范围：35-65%
   - >75%必须重做
   - <35%可接受但偏详细

3. 详略取舍（第3章）
   - 必须保留：核心概念、学说主张、法条原文、典型案例
   - 适当压缩：历史背景、论证过程
   - 可省略：过渡语句、重复举例

4. 禁止行为
   - 禁止杜撰法条、案例
   - 禁止删除中间txt文件
   - 禁止修改教材原意
"""

task = f"""
{skill_content}

【具体任务】
整理《XX法》第[X]章笔记。

工作要求：
1. 读取 sections/all_pages.txt
2. 人工切分出各小节（section1_raw.txt, section2_raw.txt...）
3. 逐节整理为 section[N].md，控制压缩率35-65%
4. 合并为完整笔记
5. 修改 md_to_html_v2.py 配置，生成HTML和PDF
6. 保留所有中间文件

工作目录：/root/.openclaw/workspace/XX法笔记/第[X]章/
"""
```

### 5.4 整理子代理流程（首次整理）

```bash
# ===== 子代理执行：首次整理第[N]章 =====

cd /root/.openclaw/workspace/XX法笔记/第[N]章/sections

# Step 1: 读取源文件确定结构（不删除任何文件）
head -100 all_pages.txt
wc -c all_pages.txt

# Step 2: 人工切分小节
# 根据"第一节、第二节..."切分
# 保存为 section1_raw.txt, section2_raw.txt...

# Step 3: 逐节整理（控制压缩率35-65%）
# 读取 section1_raw.txt → 整理为 section1.md

# Step 4: 合并所有小节
cat section*.md > XX法_第[N]章_完整笔记.md

# Step 5: 生成HTML
cd ..
# 修改 md_to_html_v2.py 中的 COURSE_NAME 和 CHAPTER_NUM
python3 md_to_html_v2.py

# Step 6: 生成PDF（必须用WeasyPrint）
weasyprint output/XX法_第[N]章_完整笔记.html output/XX法_第[N]章_完整笔记.pdf

# Step 7: 验证输出
ls -lh output/*.pdf
```

### 5.5 重新整理子代理流程

```bash
# ===== 子代理执行：重新整理第[N]章 =====

cd /root/.openclaw/workspace/XX法笔记/第[N]章

# Step 1: 备份旧文件到回收站（必须！）
backup_dir="/root/.openclaw/workspace/回收站/XX法_第[N]章_$(date +%Y%m%d_%H%M%S)"
mkdir -p "$backup_dir"
cp sections/*.md "$backup_dir/" 2>/dev/null || true
cp output/*.pdf "$backup_dir/" 2>/dev/null || true
cp output/*.html "$backup_dir/" 2>/dev/null || true
echo "已备份到: $backup_dir"

# Step 2: 删除旧文件（仅.md和PDF/HTML，保留raw.txt）
rm -f sections/*.md
rm -f sections/XX法_第[X]章_完整笔记.md
rm -f output/*.pdf
rm -f output/*.html

# Step 3-8: 同首次整理流程
```

### 5.6 大章节处理（A级章节细分）

**适用条件**：章节等级为A级，且单节内容超过400行

**细分规则**：
- 按"一、二、三..."级标题切分
- 命名格式：`section[N]_[数字].md`（如`section1_1.md`、`section1_2.md`）

**处理流程**：
```bash
cd /root/.openclaw/workspace/XX法笔记/第[N]章/sections

# 1. 读取section1_raw.txt，确定"一、二、三..."位置

# 2. 按"一、"切分为多个文件
# section1_raw.txt → section1_1_raw.txt, section1_2_raw.txt...

# 3. 分别整理 → section1_1.md, section1_2.md...

# 4. 合并（保持顺序）
cat section1_1.md section1_2.md ... section2.md section3.md > XX法_第[N]章_完整笔记.md

# 5. 生成PDF（同上）
```

### 5.7 子代理结果检查与反馈

```python
def check_and_feedback(course_name, chapter_num):
    """
    主进程检查子代理结果并反馈
    """
    chapter_dir = f"/root/.openclaw/workspace/{course_name}笔记/第{chapter_num:02d}章"
    pdf_path = f"{chapter_dir}/output/{course_name}_第{chapter_num:02d}章_完整笔记.pdf"
    
    # 1. 检查PDF是否存在
    if not os.path.exists(pdf_path):
        raise Error("PDF未生成")
    
    # 2. 计算压缩率
    # 章级压缩率
    original_pdf = glob.glob(f".../{course_name}_分章/第{chapter_num:02d}章_*.pdf")[0]
    original_pages = get_pdf_pages(original_pdf)
    note_pages = get_pdf_pages(pdf_path)
    chapter_compress = (original_pages - note_pages) / original_pages * 100
    
    # 节级压缩率
    section_stats = []
    for raw_file in glob(f"{chapter_dir}/sections/section*_raw.txt"):
        md_file = raw_file.replace("_raw.txt", ".md")
        if os.path.exists(md_file):
            raw_chars = count_chars(raw_file)
            md_chars = count_chars(md_file)
            compress = (raw_chars - md_chars) / raw_chars * 100
            section_stats.append({
                "section": os.path.basename(md_file),
                "compress": compress
            })
    
    # 3. 发送反馈
    send_wechat_message(f"""
{course_name} 第{chapter_num:02d}章 整理完成

【章级压缩率】
- 原PDF页数：{original_pages}页
- 笔记页数：  {note_pages}页
- 压缩率：    {chapter_compress:.1f}%

【节级压缩率】
""" + "\n".join([f"- {s['section']}: {s['compress']:.1f}%" for s in section_stats]))
    
    send_wechat_file(pdf_path)
    
    # 4. 判断是否重新整理
    if chapter_compress > 75:
        print(f"⚠️ 压缩率{chapter_compress:.1f}% > 75%，启动重新整理")
        spawn_redo_subagent(course_name, chapter_num)
        return False
    
    return True
```

### 5.8 质量检查清单（每章必做）

- [ ] 压缩率35-65%（禁止>75%）
- [ ] 从raw文件整理（非旧md）
- [ ] PDF用WeasyPrint生成
- [ ] 标题层级正确（#节→##一、→###（一））
- [ ] 法条用引用块
- [ ] 学说对比用表格
- [ ] 无杜撰内容

---

## 六、技术规范

### 6.1 PDF生成工具

```bash
# ✅ 正确
weasyprint input.html output.pdf

# ❌ 禁止
wkhtmltopdf input.html output.pdf  # 渲染效果不一致
```

### 6.2 md_to_html_v2.py 使用说明

**脚本位置**：`/root/.openclaw/workspace/scripts/md_to_html_v2.py`

**使用方法**：
1. 复制脚本到章目录：`cp scripts/md_to_html_v2.py 第01章/`
2. 修改配置区的 `COURSE_NAME` 和 `CHAPTER_NUM`
3. 运行：`python3 md_to_html_v2.py`

**配置示例**：
```python
# 配置区（第10-11行）
COURSE_NAME = "国际经济法"  # 课程名称
CHAPTER_NUM = "01"          # 章节编号（两位数）
```

### 6.3 LaTeX公式处理

```markdown
# ❌ 错误
$$\text{公式内容}$$

# ✅ 正确
**公式内容** 或 公式内容
```

---

## 七、常见问题速查

| 错误现象 | 原因 | 解决方案 |
|:---------|:-----|:---------|
| PDF字体不一致 | 使用不同工具生成 | 统一使用WeasyPrint |
| 压缩率>75% | 过度压缩 | 补充内容，重新整理 |
| 合并后PDF内容缺失 | 完整笔记路径错误 | 检查脚本读取路径与文件位置 |
| 公式显示为代码 | 未转换LaTeX | 转换为纯文本或加粗 |
| 缺失小节内容 | 切分边界错误 | 检查section_raw.txt的切分位置 |
| HTML生成失败 | Markdown语法错误 | 检查表格格式、代码块闭合 |
| PDF生成失败 | HTML语法错误 | 检查标签闭合、特殊字符转义 |
| 文件找不到 | 命名不规范 | 检查数字编号（01 vs 1） |

---

## 核心口诀

**删冗余不删要点，用表格不用长文，查压缩率防偷懒。**

## 版本记录

- **V0**: 定稿版（当前）
- V1-V5: 开发迭代版本（已归档）
