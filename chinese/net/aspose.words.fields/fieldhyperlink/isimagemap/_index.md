---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: Aspose.Words for .NET
description: 了解 FieldHyperlink IsImageMap 属性如何通过将坐标附加到超链接来增强服务器端图像映射，从而提高功能性。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

获取或设置是否将坐标附加到服务器端图像映射的超链接。

```csharp
public bool IsImageMap { get; set; }
```

## 例子

展示如何使用 HYPERLINK 字段链接到本地文件系统中的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，然后将光标放在指定的书签处。
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// 当我们在 Microsoft Word 中单击此 HYPERLINK 字段时，
// 它将打开链接的文档，并自动向下滚动到指定的 iframe。
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### 也可以看看

* class [FieldHyperlink](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
