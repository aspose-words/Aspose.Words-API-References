---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words for .NET
description: 使用我们的“截面克隆”方法轻松复制截面。这款强大的工具可简化您的工作流程并提高工作效率！
type: docs
weight: 130
url: /zh/net/aspose.words/section/clone/
---
## Section.Clone method

创建此部分的副本。

```csharp
public Section Clone()
```

## 例子

展示如何在文档中添加和删除章节。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// 从文档中删除第一部分。
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// 将现在第一部分的副本附加到文档末尾。
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
