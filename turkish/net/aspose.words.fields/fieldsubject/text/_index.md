---
title: FieldSubject.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: FieldSubject Text özelliğini zahmetsizce yönetin; sorunsuz veri işleme ve gelişmiş kullanıcı deneyimi için konu metninizi alın veya ayarlayın.
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

SUBJECT alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgenin "Konu" yerleşik özelliği için bir değer ayarlayın.
doc.BuiltInDocumentProperties.Subject = "My subject";

// Yerleşik özelliğin değerini görüntülemek için bir KONU alanı oluşturun.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldSubject field = (FieldSubject)builder.InsertField(FieldType.FieldSubject, true);
field.Update();

Assert.AreEqual(" SUBJECT ", field.GetFieldCode());
Assert.AreEqual("My subject", field.Result);

// SUBJECT alanının Text özellik değerini verip güncellersek, alan
// "Konu" yerleşik özelliğinin geçerli değerini, Metin özelliğinin değeriyle üzerine yaz,
// ve ardından yeni değeri göster.
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
