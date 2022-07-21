---
title: ImageFieldMergingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет данные дляImageFieldMerging./ifieldmergingcallback/imagefieldmerging событие.
type: docs
weight: 3610
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class

Предоставляет данные для[`ImageFieldMerging`](../ifieldmergingcallback/imagefieldmerging) событие.

```csharp
public class ImageFieldMergingArgs : FieldMergingArgsBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document) { get; } | Возвращает[`Document`](../fieldmergingargsbase/document) объект, для которого выполняется слияние. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname) { get; } | Получает имя поля слияния, как указано в документе. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field) { get; } | Получает объект, представляющий текущее поле слияния. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname) { get; } | Получает имя поля слияния в источнике данных. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue) { get; set; } | Получает или задает значение поля из источника данных. |
| [Image](../../aspose.words.mailmerging/imagefieldmergingargs/image) { get; set; } | Указывает изображение, которое механизм слияния должен вставить в документ. |
| [ImageFileName](../../aspose.words.mailmerging/imagefieldmergingargs/imagefilename) { get; set; } | Устанавливает имя файла изображения, которое модуль слияния должен вставить в документ. |
| [ImageHeight](../../aspose.words.mailmerging/imagefieldmergingargs/imageheight) { get; set; } | Задает высоту изображения для вставки в документ. |
| [ImageStream](../../aspose.words.mailmerging/imagefieldmergingargs/imagestream) { get; set; } | Указывает поток, из которого механизм слияния считывает изображение. |
| [ImageWidth](../../aspose.words.mailmerging/imagefieldmergingargs/imagewidth) { get; set; } | Задает ширину изображения для вставки в документ. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex) { get; } | Получает нулевой индекс объединяемой записи. |
| [Shape](../../aspose.words.mailmerging/imagefieldmergingargs/shape) { get; set; } | Указывает форму, которую механизм слияния должен вставить в документ. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename) { get; } | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |

### Примечания

Это событие происходит во время слияния, когда в документе встречается поле изображения mail merge . Вы можете отреагировать на это событие, чтобы вернуть a имя файла, поток илиImage объект почтовому механизму merge , чтобы он был вставлен в документ.

Доступны три свойства[`ImageFileName`](./imagefilename) , [`ImageStream`](./imagestream) а также[`Image`](./image) чтобы указать, откуда должно быть взято изображение. Установите только одно из этих свойств.

Чтобы вставить поле слияния изображений в документ Word, выберите команду Insert/Field, , затем выберите MergeField и введите Image:MyFieldName.

### Примеры

Показывает, как вставить изображения, хранящиеся в поле BLOB базы данных, в отчет.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Откройте средство чтения данных, которое должно быть в режиме чтения всех записей одновременно.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Ничего не делать.
    }

    /// <summary>
    /// Это вызывается, когда слияние встречает MERGEFIELD в документе с тегом «Image:» в его имени.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

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

* class [FieldMergingArgsBase](../fieldmergingargsbase)
* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
