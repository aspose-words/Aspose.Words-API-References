---
title: FieldFileName.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: 用于 .NET 的 Aspose.Words
description: FieldFileName IncludeFullPath 财产. 获取或设置是否包含完整文件路径名 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldfilename/includefullpath/
---
## FieldFileName.IncludeFullPath property

获取或设置是否包含完整文件路径名。

```csharp
public bool IncludeFullPath { get; set; }
```

## 例子

演示如何使用 FieldOptions 覆盖 FILENAME 字段的默认值。

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// 这个FILENAME字段将显示我们加载的文档的本地系统文件名。
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// 默认情况下，FILENAME 字段显示文件的名称，但不显示其完整的本地文件系统路径。
// 我们可以设置一个标志以使其显示完整的文件路径。
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// 我们还可以为此属性设置一个值
// 覆盖 FILENAME 字段显示的值。
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### 也可以看看

* class [FieldFileName](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
