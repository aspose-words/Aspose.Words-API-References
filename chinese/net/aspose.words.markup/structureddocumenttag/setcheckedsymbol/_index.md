---
title: StructuredDocumentTag.SetCheckedSymbol
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 方法. 设置用于表示复选框内容控件的选中状态的符号
type: docs
weight: 350
url: /zh/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

设置用于表示复选框内容控件的选中状态的符号。

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| characterCode | Int32 | 指定符号的字符代码。 |
| fontName | String | 包含符号的字体的名称。 |

### 评论

访问此方法仅适用于CheckboxSDT 类型。

对于所有其他 SDT 类型，将发生异常。

### 例子

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
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


