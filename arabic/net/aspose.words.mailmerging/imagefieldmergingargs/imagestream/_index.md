---
title: ImageFieldMergingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ImageFieldMergingArgs ImageStream على تعزيز دمج البريد الخاص بك من خلال دمج الصور بسلاسة للحصول على نتائج احترافية.
type: docs
weight: 40
url: /ar/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

يحدد التدفق الذي سيقرأ منه محرك دمج البريد صورة.

```csharp
public Stream ImageStream { get; set; }
```

## ملاحظات

يقوم Aspose.Words بإغلاق هذا الدفق بعد دمج الصورة في المستند.

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
        //لا تفعل شيئا.
    }

    /// <summary>
    /// يتم استدعاء هذا عندما يواجه دمج البريد MERGEFIELD في المستند مع علامة "Image:" في اسمه.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### أنظر أيضا

* class [ImageFieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
