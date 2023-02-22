---
title: MailMerge.GetFieldNames
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Belgede bulunan adres mektup birleştirme alan adlarının bir koleksiyonunu döndürür.
type: docs
weight: 220
url: /tr/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Belgede bulunan adres mektup birleştirme alan adlarının bir koleksiyonunu döndürür.

```csharp
public string[] GetFieldNames()
```

### Notlar

İsteğe bağlı önek dahil tam birleştirme alan adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Her çağrıda yeni bir string[] dizisi oluşturulur.

Aşağıdaki durumlarda "bıyık" alan adlarını içerir:[`UseNonMergeFields`](../usenonmergefields/) dır-dir **doğru**.

### Örnekler

Bir belgedeki tüm birleştirme alanlarının adlarının nasıl alınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// Belgedeki her MERGEFIELD adı için veri tablosunun bir sütun içerdiğinden emin olun
// aynı ada sahip ve ardından adres mektup birleştirmeyi yürütün. 
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


