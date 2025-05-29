---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words for .NET
description: 探索 Range UnlinkFields 方法，轻松取消文档范围内字段的链接，增强您的工作流程和文档管理。
type: docs
weight: 120
url: /zh/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

取消此范围内的字段链接。

```csharp
public void UnlinkFields()
```

## 评论

用最新的结果替换此范围内的所有字段。

要取消整个文档中的字段链接，请使用`UnlinkFields`。

## 例子

显示如何取消某个范围内的所有字段的链接。

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
