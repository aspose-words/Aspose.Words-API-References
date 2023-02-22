---
title: ImageFieldMergingArgs.ImageWidth
second_title: Справочник по API Aspose.Words для .NET
description: ImageFieldMergingArgs свойство. Задает ширину изображения для вставки в документ.
type: docs
weight: 50
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/imagewidth/
---
## ImageFieldMergingArgs.ImageWidth property

Задает ширину изображения для вставки в документ.

```csharp
public MergeFieldImageDimension ImageWidth { get; set; }
```

### Примечания

Значение этого свойства исходно исходит из соответствующего кода MERGEFIELD, содержащегося в документе шаблона . Чтобы переопределить начальное значение, вы должны назначить экземпляр [`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) class к этому свойству или установите свойства для instance из[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) класс, возвращаемый этим свойством.

Чтобы указать, что исходное значение ширины изображения должно быть применено, вы должны назначить **нулевой** этому свойству или установите[`Value`](../../../aspose.words.fields/mergefieldimagedimension/value/) свойство для instance из[`MergeFieldImageDimension`](../../../aspose.words.fields/mergefieldimagedimension/) класс, возвращаемый этим свойством, к отрицательному значению.

### Примеры

Показывает, как установить размеры изображений, поскольку MERGEFIELDS принимает их во время слияния.

```csharp
{
    Document doc = new Document();

    // Вставьте MERGEFIELD, которое будет принимать изображения из источника во время слияния почты. Используйте код поля для ссылки
    // столбец в источнике данных, содержащий локальные системные имена файлов изображений, которые мы хотим использовать при слиянии.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // В источнике данных должен быть такой столбец с именем "ImageColumn".
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Создадим подходящий источник данных.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Настройте обратный вызов для изменения размеров изображений во время слияния, затем выполните слияние.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");

/// <summary>
/// Устанавливает размер всех изображений, объединенных почтой, в одну определенную ширину и высоту.
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
* пространство имен [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* сборка [Aspose.Words](../../../)


