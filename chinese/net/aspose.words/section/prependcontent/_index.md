---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: 用于 .NET 的 Aspose.Words
description: Section PrependContent 方法. 在本节的开头插入源节内容的副本 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

在本节的开头插入源节内容的副本。

```csharp
public void PrependContent(Section sourceSection)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sourceSection | Section | 从中复制内容的部分。 |

## 评论

仅内容[`Body`](../body/)复制源部分的内容，不复制页面设置、 页眉和页脚。

如果源部分属于不同的文档，则会自动导入节点。

目标文档中不会创建新部分。

## 例子

演示如何将一个部分的内容附加到另一个部分。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// 将第一部分的内容插入到第三部分的开头。
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// 将第二部分的内容插入到第三部分的末尾。
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// “PrependContent”和“AppendContent”方法没有创建任何新部分。
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### 也可以看看

* class [Section](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
