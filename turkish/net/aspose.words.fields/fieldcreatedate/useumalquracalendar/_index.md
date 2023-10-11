---
title: FieldCreateDate.UseUmAlQuraCalendar
second_title: Aspose.Words for .NET API Referansı
description: FieldCreateDate mülk. UmalQura takviminin kullanılıp kullanılmayacağını alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldcreatedate/useumalquracalendar/
---
## FieldCreateDate.UseUmAlQuraCalendar property

Um-al-Qura takviminin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseUmAlQuraCalendar { get; set; }
```

### Örnekler

Belgenin oluşturulma tarihini/saatini görüntülemek için CREATEDATE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Belgenin oluşturulma tarihini ve saatini görüntülemek için CREATEDATE alanını kullanabiliriz.
// Aşağıda CREATEDATE alanının tarih/saati görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 - İslami Ay Takvimi:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Ümmü'l-Kura takvimi:
builder.Write("\nAccording to the Umm al-Qura Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\u", field.GetFieldCode());

// 3 - Hindistan Ulusal Takvimi:
builder.Write("\nAccording to the Indian National Calendar - ");
field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" CREATEDATE  \\s", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CREATEDATE.docx");
```

### Ayrıca bakınız

* class [FieldCreateDate](../)
* ad alanı [Aspose.Words.Fields](../../fieldcreatedate/)
* toplantı [Aspose.Words](../../../)


