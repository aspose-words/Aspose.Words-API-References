---
title: ImageFieldMergingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ImageFieldMergingArgs ImageStream улучшает процесс слияния писем за счет бесшовной интеграции изображений для получения профессиональных результатов.
type: docs
weight: 40
url: /ru/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

Указывает поток, из которого механизм слияния почты будет считывать изображение.

```csharp
public Stream ImageStream { get; set; }
```

## Примечания

Aspose.Words закрывает этот поток после объединения изображения с документом.

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

        // Откройте средство чтения данных, которое должно находиться в режиме, позволяющем считывать все записи одновременно.
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
    /// Вызывается, когда при слиянии почты в документе обнаруживается MERGEFIELD с тегом «Image:» в имени.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Смотрите также

* class [ImageFieldMergingArgs](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
