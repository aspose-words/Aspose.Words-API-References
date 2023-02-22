---
title: ImageFieldMergingArgs.Image
second_title: Справочник по API Aspose.Words для .NET
description: ImageFieldMergingArgs свойство. Указывает изображение которое механизм слияния должен вставить в документ.
type: docs
weight: 10
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/image/
---
## ImageFieldMergingArgs.Image property

Указывает изображение, которое механизм слияния должен вставить в документ.

```csharp
public Image Image { get; set; }
```

### Примеры

Показывает, как использовать обратный вызов для настройки логики слияния изображений.

```csharp
{
    Document doc = new Document();

    // Вставьте MERGEFIELD, которое будет принимать изображения из источника во время слияния почты. Используйте код поля для ссылки
    // столбец в источнике данных, который содержит локальные системные имена файлов изображений, которые мы хотим использовать при слиянии.
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldMergeField field = (FieldMergeField)builder.InsertField("MERGEFIELD Image:ImageColumn");

    // В этом случае поле ожидает, что источник данных будет иметь такой столбец с именем «ImageColumn».
    Assert.AreEqual("Image:ImageColumn", field.FieldName);

    // Имена файлов могут быть длинными, и если мы сможем найти способ избежать их хранения в источнике данных,
    // мы можем значительно уменьшить его размер.
    // Создаем источник данных, который ссылается на изображения, используя короткие имена.
    DataTable dataTable = new DataTable("Images");
    dataTable.Columns.Add(new DataColumn("ImageColumn"));
    dataTable.Rows.Add("Dark logo");
    dataTable.Rows.Add("Transparent logo");

    // Назначить объединяющий обратный вызов, который содержит всю логику, обрабатывающую эти имена,
     // и затем выполнить слияние почты.
    doc.MailMerge.FieldMergingCallback = new ImageFilenameCallback();
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "Field.MERGEFIELD.Images.docx");

/// <summary>
/// Содержит словарь, который сопоставляет имена изображений с именами файлов локальной системы, которые содержат эти изображения.
/// Если источник данных слияния использует одно из имен словаря для ссылки на изображение,
/// этот обратный вызов передаст соответствующее имя файла в место назначения слияния.
/// </summary>
private class ImageFilenameCallback : IFieldMergingCallback
{
    public ImageFilenameCallback()
    {
        mImageFilenames = new Dictionary<string, string>();
        mImageFilenames.Add("Dark logo", ImageDir + "Logo.jpg");
        mImageFilenames.Add("Transparent logo", ImageDir + "Transparent background logo.png");
    }

    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        throw new NotImplementedException();
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        if (mImageFilenames.ContainsKey(args.FieldValue.ToString()))
        {
            #if NET48 || JAVA
            args.Image = Image.FromFile(mImageFilenames[args.FieldValue.ToString()]);
            #elif NET5_0_OR_GREATER
            args.Image = SKBitmap.Decode(mImageFilenames[args.FieldValue.ToString()]);
            args.ImageFileName = mImageFilenames[args.FieldValue.ToString()];
            #endif
        }

        Assert.NotNull(args.Image);
    }

    private readonly Dictionary<string, string> mImageFilenames;
}
```

### Смотрите также

* class [ImageFieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* сборка [Aspose.Words](../../../)


