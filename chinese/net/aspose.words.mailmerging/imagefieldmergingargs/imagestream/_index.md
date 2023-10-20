---
title: ImageFieldMergingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: 用于 .NET 的 Aspose.Words
description: ImageFieldMergingArgs ImageStream 财产. 指定邮件合并引擎从中读取图像的流 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.mailmerging/imagefieldmergingargs/imagestream/
---
## ImageFieldMergingArgs.ImageStream property

指定邮件合并引擎从中读取图像的流。

```csharp
public Stream ImageStream { get; set; }
```

## 评论

Aspose.Words 在将图像合并到文档中后关闭此流。

## 例子

演示如何将存储在数据库 BLOB 字段中的图像插入到报表中。

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

        // 打开数据读取器，需要处于一次读取所有记录的模式。
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
        // 没做什么。
    }

    /// <summary>
    /// 当邮件合并在文档中遇到名称中包含“Image:”标记的 MERGEFIELD 时，将调用此函数。
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### 也可以看看

* class [ImageFieldMergingArgs](../)
* 命名空间 [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../../)
