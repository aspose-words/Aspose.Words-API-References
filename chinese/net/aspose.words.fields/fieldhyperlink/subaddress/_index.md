---
title: FieldHyperlink.SubAddress
second_title: Aspose.Words for .NET API 参考
description: FieldHyperlink 财产. 获取或设置文件中此超链接跳转的位置例如书签
type: docs
weight: 60
url: /zh/net/aspose.words.fields/fieldhyperlink/subaddress/
---
## FieldHyperlink.SubAddress property

获取或设置文件中此超链接跳转的位置，例如书签。

```csharp
public string SubAddress { get; set; }
```

### 例子

演示如何使用 HYPERLINK 字段链接到本地文件系统中的文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// 当我们在 Microsoft Word 中单击此超链接字段时，
// 它将打开链接的文档，然后将光标置于指定的书签处。
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// 当我们在 Microsoft Word 中单击此超链接字段时，
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
* 命名空间 [Aspose.Words.Fields](../../fieldhyperlink/)
* 部件 [Aspose.Words](../../../)


