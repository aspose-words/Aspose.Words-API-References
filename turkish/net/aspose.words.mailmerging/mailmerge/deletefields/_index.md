---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: .NET için Aspose.Words
description: MailMerge DeleteFields yöntemiyle belgelerinizi zahmetsizce düzene sokarak gereksiz posta birleştirme alanlarını kaldırarak daha temiz, daha profesyonel sonuçlar elde edin.
type: docs
weight: 170
url: /tr/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

Belgeden posta birleştirmeyle ilgili alanları kaldırır.

```csharp
public void DeleteFields()
```

## Notlar

Bu yöntem MERGEFIELD ve NEXT alanlarını belgeden kaldırır.

Bu yöntem, posta birleştirme işleminizin belgedeki tüm alanları doldurması için her zaman 'ye ihtiyaç duymaması durumunda yararlı olabilir. Bu yöntemi, kalan tüm posta birleştirme alanlarını kaldırmak için kullanın.

## Örnekler

Bir belgeden tüm MERGEFIELD'lerin nasıl silineceğini gösterir.

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
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
