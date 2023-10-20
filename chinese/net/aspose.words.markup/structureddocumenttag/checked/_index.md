---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag Checked 财产. 获取/设置复选框的当前状态SDT. 此属性的默认值为 false 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

获取/设置复选框的当前状态**SDT**. 此属性的默认值为 false。

```csharp
public bool Checked { get; set; }
```

## 评论

访问此属性仅适用于Checkbox SDT 类型。

对于所有其他 SDT 类型，将发生异常。

## 例子

展示如何以复选框的形式创建结构化文档标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// 我们可以设置用于表示复选框内容控件的选中/未选中状态的符号。
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
