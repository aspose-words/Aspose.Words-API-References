---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: 用于 .NET 的 Aspose.Words
description: FieldGoToButton DisplayText 财产. 获取或设置出现在文档中的按钮的文本以便可以选择它来激活跳转 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

获取或设置出现在文档中的“按钮”的文本，以便可以选择它来激活跳转。

```csharp
public string DisplayText { get; set; }
```

## 例子

显示插入 GOTOBUTTON 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 添加 GOTOBUTTON 字段。当我们在 Microsoft Word 中双击该字段时，
// 它将把文本光标移至 Location 属性引用其名称的书签。
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// 为要引用的字段插入有效书签。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### 也可以看看

* class [FieldGoToButton](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
