---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: 用于 .NET 的 Aspose.Words
description: Range UnlinkFields 方法. 取消链接此范围内的字段 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

取消链接此范围内的字段。

```csharp
public void UnlinkFields()
```

## 评论

将此范围内的所有字段替换为其最新结果。

要取消链接整个文档中的字段，请使用`UnlinkFields`。

## 例子

展示如何取消链接范围内的所有字段。

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### 也可以看看

* class [Range](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
