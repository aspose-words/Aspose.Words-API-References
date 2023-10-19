---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: FieldSubject Text mülk. Konunun metnini alır veya ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldsubject/text/
---
## FieldSubject.Text property

Konunun metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
```

## Örnekler

KONU alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgenin "Konu" yerleşik özelliği için bir değer belirleyin.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Bu yerleşik özelliğin değerini görüntülemek için bir SUBJECT alanı oluşturun.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// SUBJECT alanının Text özelliği değerini verip güncellersek alan şu şekilde olacaktır:
// "Subject" yerleşik özelliğinin mevcut değerinin üzerine Text özelliğinin değerini yazın,
// ve ardından yeni değeri görüntüleyin.
field.Text = "My new subject";
field.Update();

Assert.AreEqual(" SUBJECT  \"My new subject\"", field.GetFieldCode());
Assert.AreEqual("My new subject", field.Result);

Assert.AreEqual("My new subject", doc.BuiltInDocumentProperties.Subject);

doc.Save(ArtifactsDir + "Field.SUBJECT.docx");
```

### Ayrıca bakınız

* class [FieldSubject](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
