---
title: ImageFieldMergingArgs.ImageHeight
linktitle: ImageHeight
articleTitle: ImageHeight
second_title: Aspose.Words для .NET
description: ImageFieldMergingArgs ImageHeight свойство. Указывает высоту изображения для вставки в документ на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/imageheight/
---
## ImageFieldMergingArgs.ImageHeight property

Указывает высоту изображения для вставки в документ.

```csharp
public MergeFieldImageDimension ImageHeight { get; set; }
```

## Примечания

Значение этого свойства изначально берется из соответствующего кода MERGEFIELD, содержащегося в документе шаблона . Чтобы переопределить начальное значение, вам следует назначить экземпляр [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) класс для этого свойства или установите свойства для экземпляра экземпляра [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) класс, возвращаемый этим свойством.

Чтобы указать, что должно быть применено исходное значение высоты изображения, вам следует присвоить`нулевой` для этого свойства или установите[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) свойство для экземпляра из[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) class, возвращаемый этим свойством, имеет отрицательное значение.

## Примеры

Показывает, как установить размеры изображений, поскольку MERGEFIELDS принимает их во время слияния почты.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Вставляем MERGEFIELD, который будет принимать изображения из источника во время слияния почты. Используйте код поля для ссылки
    // столбец в источнике данных, содержащий имена локальных системных файлов изображений, которые мы хотим использовать при слиянии писем.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Источник данных должен иметь такой столбец с именем «ImageColumn».
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Создаем подходящий источник данных.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Настройте обратный вызов для изменения размеров изображений во время слияния, а затем выполните слияние почты.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Устанавливает размер всех объединенных изображений почты в одну определенную ширину и высоту.
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

### Смотрите также

* class [MergeFieldImageDimension](../../../aspose.words.fields/mergefieldimagedimension/)
* class [ImageFieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
