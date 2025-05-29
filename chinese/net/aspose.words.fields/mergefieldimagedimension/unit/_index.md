---
title: MergeFieldImageDimension.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words for .NET
description: 探索 MergeFieldImageDimension Unit 属性，实现精确的图像缩放。通过精确的尺寸和更佳的视觉吸引力，提升您的设计。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/mergefieldimagedimension/unit/
---
## MergeFieldImageDimension.Unit property

单位。

```csharp
public MergeFieldImageDimensionUnit Unit { get; set; }
```

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

* enum [MergeFieldImageDimensionUnit](../../mergefieldimagedimensionunit/)
* class [MergeFieldImageDimension](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
