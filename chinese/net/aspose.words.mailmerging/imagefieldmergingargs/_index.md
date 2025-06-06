---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMerging.ImageFieldMergingArgs 类，旨在增强文档中的图像合并，确保无缝高效的工作流程。
type: docs
weight: 4520
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

为[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/)事件.

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | 返回[`Document`](../fieldmergingargsbase/document/)执行邮件合并的对象。 |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | 获取文档中指定的合并字段的名称。 |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | 获取代表当前合并字段的对象。 |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | 获取数据源中合并字段的名称。 |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | 从数据源获取或设置字段的值。 |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | 指定邮件合并引擎必须插入到文档中的图像。 |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | 设置邮件合并引擎必须插入文档的图像的文件名。 |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | 指定插入文档的图像高度。 |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | 指定邮件合并引擎读取图像的流。 |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | 指定插入文档的图像宽度。 |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | 获取正在合并的记录的从零开始的索引。 |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | 指定邮件合并引擎必须插入到文档中的形状。 |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | 获取当前合并操作的数据表名称，如果名称不可用，则获取空字符串。 |

## 评论

邮件合并期间，当文档中遇到图像邮件合并 字段时，会发生此事件。您可以响应此事件以返回 文件名、流或Image对象到邮件merge 引擎，以便将其插入到文档中。

有三处房产可供选择[`ImageFileName`](./imagefilename/), [`ImageStream`](./imagestream/)和[`Image`](./image/)指定必须从哪里获取图像。 仅设置其中一个属性。

要在 Word 文档中插入图像邮件合并字段，请选择“插入/字段”命令， ，然后选择“合并字段”并键入“Image:MyFieldName”。

## 例子

展示如何将存储在数据库 BLOB 字段中的图像插入到报告中。

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.ACE.OLEDB.12.0;Data Source={DatabaseDir + "Northwind.accdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // 打开数据读取器，需要处于一次读取所有记录的模式。
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");
}

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // 什么也不做。
    }

    /// <summary>
    /// 当邮件合并在文档中遇到名称中带有“Image:”标签的 MERGEFIELD 时调用此函数。
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

展示如何在邮件合并期间设置 MERGEFIELDS 接受的图像尺寸。

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // 插入一个合并字段，用于在邮件合并期间接收来自源的图片。使用字段代码来引用
    // 数据源中的一列包含我们希望在邮件合并中使用的图像的本地系统文件名。
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // 数据源应该有一个名为“ImageColumn”的列。
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // 创建合适的数据源。
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // 配置回调以在合并时修改图像的大小，然后执行邮件合并。
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// 将所有邮件合并图像的大小设置为一个定义的宽度和高度。
/// </summary>
private class MergedImageResizer : IFieldMergingCallback
{
    public MergedImageResizer(double imageWidth, double imageHeight, MergeFieldImageDimensionUnit unit)
    {
        mImageWidth = imageWidth;
        mImageHeight = imageHeight;
        mUnit = unit;
    }

    public void FieldMerging(FieldMergingArgs e)
    {
        throw new NotImplementedException();
    }

    public void ImageFieldMerging(ImageFieldMergingArgs args)
    {
        args.ImageFileName = args.FieldValue.ToString();
        args.ImageWidth = new MergeFieldImageDimension(mImageWidth, mUnit);
        args.ImageHeight = new MergeFieldImageDimension(mImageHeight, mUnit);

        Assert.AreEqual(mImageWidth, args.ImageWidth.Value);
        Assert.AreEqual(mUnit, args.ImageWidth.Unit);
        Assert.AreEqual(mImageHeight, args.ImageHeight.Value);
        Assert.AreEqual(mUnit, args.ImageHeight.Unit);
        Assert.Null(args.Shape);
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### 也可以看看

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
