---
title: ImageFieldMergingArgs.ImageWidth
linktitle: ImageWidth
articleTitle: ImageWidth
second_title: Aspose.Words for .NET
description: 调整 ImageFieldMergingArgs 中的 ImageWidth 以将图像无缝插入到您的文档中，增强视觉吸引力和布局。
type: docs
weight: 50
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

指定插入文档的图像宽度。

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

## 评论

此属性的初始值来自 模板文档中相应的 MERGEFIELD 代码。要覆盖初始值，您应该分配一个 实例[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)类到此属性或设置instance 的属性[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)类，由此属性返回。

为指示应应用图像宽度的原始值，应分配`无效的` 值添加到此属性或设置[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/)的实例 的属性[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/)类，由此属性返回，为负值。

## 例子

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

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
