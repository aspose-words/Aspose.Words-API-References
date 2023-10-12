---
title: MailMerge.DeleteFields
second_title: Aspose.Words for .NET API Referansı
description: MailMerge yöntem. Adresmektup birleştirmeyle ilgili alanları belgeden kaldırır.
type: docs
weight: 170
url: /tr/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Adres-mektup birleştirmeyle ilgili alanları belgeden kaldırır.

```csharp
public void DeleteFields()
```

### Notlar

Bu yöntem, MERGEFIELD ve NEXT alanlarını belgeden kaldırır.

Adres-mektup birleştirme işleminiz belgedeki tüm alanları doldurmak için her zaman 'ye ihtiyaç duymuyorsa bu yöntem yararlı olabilir. Kalan adres-mektup birleştirme alanlarının tümünü kaldırmak için bu yöntemi kullanın.

### Örnekler

Bir belgedeki tüm MERGEFIELD'lerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


