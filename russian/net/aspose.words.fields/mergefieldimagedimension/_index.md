---
title: MergeFieldImageDimension Class
linktitle: MergeFieldImageDimension
articleTitle: MergeFieldImageDimension
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.MergeFieldImageDimension для точного определения размера изображений в почтовых слияниях. Улучшите автоматизацию документов сегодня!
type: docs
weight: 3160
url: /ru/net/aspose.words.fields/mergefieldimagedimension/
---
## MergeFieldImageDimension class

Представляет размер изображения (т. е. ширину или высоту), используемый в процессе слияния почты.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class MergeFieldImageDimension
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor)(*double*) | Создает экземпляр размера изображения с заданным значением в точках. |
| [MergeFieldImageDimension](mergefieldimagedimension/#constructor_1)(*double, [MergeFieldImageDimensionUnit](../mergefieldimagedimensionunit/)*) | Создает экземпляр размера изображения с заданным значением и заданной единицей измерения. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Unit](../../aspose.words.fields/mergefieldimagedimension/unit/) { get; set; } | Единица измерения. |
| [Value](../../aspose.words.fields/mergefieldimagedimension/value/) { get; set; } | Значение. |

## Примечания

Чтобы указать, что изображение должно быть вставлено с исходным размером во время слияния почты, следует присвоить отрицательное значение[`Value`](./value/) свойство.

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
