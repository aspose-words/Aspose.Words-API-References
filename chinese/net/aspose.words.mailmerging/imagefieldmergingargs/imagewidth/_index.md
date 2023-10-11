---
title: ImageFieldMergingArgs.ImageWidth
second_title: Aspose.Words for .NET API 参考
description: ImageFieldMergingArgs 财产. 指定要插入到文档中的图像的图像宽度
type: docs
weight: 50
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

指定要插入到文档中的图像的图像宽度。

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

### 评论

该属性的值最初来自相应的 MERGEFIELD 代码，包含在 模板文档中。要覆盖初始值，您应该分配一个实例 of [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)类为此属性或设置实例 的属性[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)类，由此属性返回。

要指示应应用图像宽度的原始值，您应该分配`无效的` 值为此属性或设置[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/)的instance 的属性[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)该属性返回的类为负值。

### 例子

展示如何在 MERGEFIELDS 在邮件合并期间接受图像时设置图像尺寸。

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // 插入一个 MERGEFIELD，它将在邮件合并期间接受来自源的图像。使用字段代码来引用
    // 数据源中的一列，包含我们希望在邮件合并中使用的图像的本地系统文件名。
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
    }

    private readonly double mImageWidth;
    private readonly double mImageHeight;
    private readonly MergeFieldImageDimensionUnit mUnit;
}
```

### 也可以看看

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* 部件 [Aspose.Words](../../../)


