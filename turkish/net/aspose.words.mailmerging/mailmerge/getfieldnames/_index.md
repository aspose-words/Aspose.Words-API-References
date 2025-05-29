---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: .NET için Aspose.Words
description: Belgenizdeki tüm posta birleştirme alan adlarına zahmetsizce erişmek ve bunları kullanmak için MailMerge GetFieldNames yöntemini keşfedin ve belge otomasyonunu kolaylaştırın.
type: docs
weight: 220
url: /tr/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Belgede bulunan birleştirme alanı adlarının bir koleksiyonunu döndürür.

```csharp
public string[] GetFieldNames()
```

## Notlar

İsteğe bağlı önek dahil olmak üzere tam birleştirme alanı adlarını döndürür. Yinelenen alan adlarını ortadan kaldırmaz.

Her çağrıda yeni bir dize dizisi oluşturulur.

Eğer "bıyık" alan adlarını içeriyorsa[`UseNonMergeFields`](../usenonmergefields/) dır`doğru`.

## Örnekler

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

// Belgedeki her MERGEFIELD adı için, veri tablosunun bir sütun içerdiğinden emin olun
 // aynı adı taşıyın ve ardından posta birleştirmeyi gerçekleştirin.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
