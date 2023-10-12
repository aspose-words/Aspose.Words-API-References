---
title: LoadOptions.PreserveIncludePictureField
second_title: Aspose.Words for .NET API 参考
description: LoadOptions 财产. 获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段 默认值为错误的.
type: docs
weight: 120
url: /zh/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 默认值为`错误的`.

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### 评论

默认情况下，INCLUDEPICTURE 字段会转换为形状对象。如果您需要保留字段（例如，如果您希望以编程方式更新它），则可以覆盖该字段。但请注意，this 方法对于 Aspose.Words 并不常见。自行承担使用风险。

可能的用例之一可能是使用 MERGEFIELD 作为子字段来动态更改图片的源 path 。在这种情况下，您需要将 INCLUDEPICTURE 保留在模型中。

### 例子

演示如何在加载文档时保留或丢弃 INCLUDEPICTURE 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // 我们可以在 LoadOptions 对象中设置一个标志来决定是否转换所有 INCLUDEPICTURE 字段
    // 加载包含图像形状的文档时将其转换为图像形状。
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../loadoptions/)
* 部件 [Aspose.Words](../../../)


