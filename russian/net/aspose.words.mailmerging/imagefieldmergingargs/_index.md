---
title: ImageFieldMergingArgs Class
linktitle: ImageFieldMergingArgs
articleTitle: ImageFieldMergingArgs
second_title: Aspose.Words для .NET
description: Aspose.Words.MailMerging.ImageFieldMergingArgs сорт. Предоставляет данные дляImageFieldMerging событие на С#.
type: docs
weight: 3830
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Предоставляет данные для[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging/) событие.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | Возвращает[`Document`](../fieldmergingargsbase/document/) объект, для которого выполняется слияние почты. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | Получает имя поля слияния, указанное в документе. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | Получает объект, представляющий текущее поле слияния. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | Получает имя поля слияния в источнике данных. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | Получает или задает значение поля из источника данных. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image/) { get; set; } | Указывает изображение, которое механизм слияния почты должен вставить в документ. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename/) { get; set; } | Устанавливает имя файла изображения, которое механизм слияния почты должен вставить в документ. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight/) { get; set; } | Указывает высоту изображения для вставки в документ. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream/) { get; set; } | Указывает поток, из которого механизм слияния почты читает изображение. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth/) { get; set; } | Указывает ширину изображения для вставки в документ. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | Получает индекс объединяемой записи, начинающийся с нуля. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape/) { get; set; } | Указывает форму, которую механизм слияния почты должен вставить в документ. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |

## Примечания

Это событие происходит во время слияния почты, когда в документе встречается поле изображения mail merge . Вы можете отреагировать на это событие, чтобы вернуть имя файла, поток или поток a .Image объект почтовому механизму merge , чтобы он был вставлен в документ.

Доступны три объекта недвижимости[`ImageFileName`](./imagefilename/) , [`ImageStream`](./imagestream/) и[`Image`](./image/) чтобы указать, откуда должно быть взято изображение. Установите только одно из этих свойств.

Чтобы вставить поле слияния изображения в документ Word, выберите команду «Вставить/Поле», , затем выберите «MergeField» и введите «Image:MyFieldName».

## Примеры

Показывает, как вставлять в отчет изображения, хранящиеся в BLOB-поле базы данных.

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

        // Открытие устройства чтения данных, которое должно находиться в режиме одновременного чтения всех записей.
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
        // Ничего не делать.
    }

    /// <summary>
    /// Это вызывается, когда слияние почты обнаруживает в документе MERGEFIELD с тегом «Image:» в его имени.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
