---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words for .NET
description: 使用 FieldFileSize 的 IsInMegabytes 属性控制文件大小的显示。轻松在字节和兆字节之间切换，以获得更清晰的显示效果和更好的用户体验。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

获取或设置是否以兆字节显示文件大小。

```csharp
public bool IsInMegabytes { get; set; }
```

## 例子

展示如何使用 FILESIZE 字段显示文档的文件大小。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// 以下是三种不同的计量单位
// 使用FILESIZE字段可以显示文档的文件大小。
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
// 我们必须先保存更改，然后手动更新这些字段。
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### 也可以看看

* class [FieldFileSize](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
