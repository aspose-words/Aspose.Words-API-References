---
title: ImageFieldMergingArgs.Shape
linktitle: Shape
articleTitle: Shape
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ImageFieldMergingArgs Shape улучшает ваши документы слияния, позволяя точно вставлять фигуры для придания им изысканного вида.
type: docs
weight: 60
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Указывает форму, которую механизм слияния почты должен вставить в документ.

```csharp
public Shape Shape { get; set; }
```

## Примечания

Если указано это свойство, механизм слияния почты игнорирует все другие свойства, такие как[`ImageFileName`](../imagefilename/) или[`ImageStream`](../imagestream/) и просто вставляет фигуру в документ.

Используйте это свойство для полного управления процессом слияния поля слияния изображений. Например, вы можете указать[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/)или любое другое свойство формы для точной настройки результирующего узла. Однако, обратите внимание, что вы несете ответственность за предоставление содержимого формы.

## Примеры

Показывает, как задать размеры изображений, поскольку MERGEFIELDS принимает их во время слияния почты.

```csharp
public void MergeFieldImageDimension()
{
    Document doc = new Document();

    // Вставьте MERGEFIELD, который будет принимать изображения из источника во время слияния почты. Используйте код поля для ссылки
    // столбец в источнике данных, содержащий локальные системные имена файлов изображений, которые мы хотим использовать при слиянии.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // Источник данных должен иметь такой столбец с именем «ImageColumn».
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Создайте подходящий источник данных.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add(ImageDir + "Logo.jpg");
    dataTable.Rows.Add(ImageDir + "Transparent background logo.png");
    dataTable.Rows.Add(ImageDir + "Enhanced Windows MetaFile.emf");

    // Настройте обратный вызов для изменения размеров изображений во время слияния, затем выполните слияние почты.
    doc.MailMerge.FieldMergingCallback = new MergedImageResizer(200, 200, MergeFieldImageDimensionUnit.Point);
    doc.MailMerge.Execute(dataTable);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.MERGEFIELD.ImageDimension.docx");
}

/// <summary>
/// Устанавливает размер всех объединенных изображений на одну определенную ширину и высоту.
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

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
