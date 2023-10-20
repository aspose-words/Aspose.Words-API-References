---
title: IFieldMergingCallback.ImageFieldMerging
linktitle: ImageFieldMerging
articleTitle: ImageFieldMerging
second_title: Aspose.Words لـ .NET
description: IFieldMergingCallback ImageFieldMerging طريقة. يتم استدعاؤه عندما يكون محرك دمج البريد Aspose.Words على وشك إدراج صورة في حقل دمج في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.mailmerging/ifieldmergingcallback/imagefieldmerging/
---
## IFieldMergingCallback.ImageFieldMerging method

يتم استدعاؤه عندما يكون محرك دمج البريد Aspose.Words على وشك إدراج صورة في حقل دمج.

```csharp
public void ImageFieldMerging(ImageFieldMergingArgs args)
```

## أمثلة

يوضح كيفية إدراج الصور المخزنة في حقل BLOB بقاعدة البيانات في تقرير.

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

        // افتح قارئ البيانات، والذي يجب أن يكون في وضع يقرأ جميع السجلات مرة واحدة.
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
        // لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج البريد MERGEFIELD في المستند الذي يحتوي على علامة "صورة:" في اسمه.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### أنظر أيضا

* class [ImageFieldMergingArgs](../../imagefieldmergingargs/)
* interface [IFieldMergingCallback](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
