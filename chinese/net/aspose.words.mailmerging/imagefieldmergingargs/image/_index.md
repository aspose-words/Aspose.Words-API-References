---
title: ImageFieldMergingArgs.Image
linktitle: Image
articleTitle: Image
second_title: 用于 .NET 的 Aspose.Words
description: ImageFieldMergingArgs Image 财产. 指定邮件合并引擎必须插入到文档中的图像 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

指定邮件合并引擎必须插入到文档中的图像。

```csharp
public Image Image { get; set; }
```

## 例子

演示如何使用回调来自定义图像合并逻辑。

```csharp
public void MergeFieldImages()
{
    Document doc = new Document();

    // 插入一个 MERGEFIELD，它将在邮件合并期间接受来自源的图像。使用字段代码来引用
    // 数据源中的一列，其中包含我们希望在邮件合并中使用的图像的本地系统文件名。
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // 在本例中，该字段期望数据源具有这样一个名为“ImageColumn”的列。
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // 文件名可能很长，如果我们能找到一种方法来避免将它们存储在数据源中，
    // 我们可以大大减小它的大小。
    // 创建一个使用短名称引用图像的数据源。
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // 分配一个合并回调，其中包含处理这些名称的所有逻辑，
     // 然后执行邮件合并。
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");
}

/// <summary>
/// 包含一个字典，将图像名称映射到包含这些图像的本地系统文件名。
/// 如果邮件合并数据源使用字典的名称之一来引用图像，
/// 此回调会将相应的文件名传递到合并目标。
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET48 || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### 也可以看看

* class [ImageFieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
