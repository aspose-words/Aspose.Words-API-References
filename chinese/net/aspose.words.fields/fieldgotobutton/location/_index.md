---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: 用于 .NET 的 Aspose.Words
description: FieldGoToButton Location 财产. 获取或设置书签的名称页码或要跳转到的其他项目 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

获取或设置书签的名称、页码或要跳转到的其他项目。

```csharp
public string Location { get; set; }
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
