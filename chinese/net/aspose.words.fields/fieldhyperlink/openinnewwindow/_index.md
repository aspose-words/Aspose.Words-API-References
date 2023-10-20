---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: 用于 .NET 的 Aspose.Words
description: FieldHyperlink OpenInNewWindow 财产. 获取或设置是否在新的 Web 浏览器窗口中打开目标站点 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

获取或设置是否在新的 Web 浏览器窗口中打开目标站点。

```csharp
public bool OpenInNewWindow { get; set; }
```

## 例子

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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
