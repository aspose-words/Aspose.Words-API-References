---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: 用于 .NET 的 Aspose.Words
description: FieldFileSize IsInKilobytes 财产. 获取或设置是否以千字节为单位显示文件大小 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

获取或设置是否以千字节为单位显示文件大小。

```csharp
public bool IsInKilobytes { get; set; }
```

## 例子

演示如何使用 FILESIZE 字段显示文档的文件大小。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// 下面是三种不同的测量单位
// FILESIZE 字段可以显示文档的文件大小。
// 1 - 字节：
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - 千字节：
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - 兆字节：
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// 要在 Microsoft Word 中编辑时更新这些字段的值，
// 我们必须首先保存更改，然后手动更新这些字段。
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### 也可以看看

* class [FieldFileSize](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
