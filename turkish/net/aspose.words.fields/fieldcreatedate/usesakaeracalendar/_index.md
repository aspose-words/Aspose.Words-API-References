---
title: FieldCreateDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: .NET için Aspose.Words
description: Uygulamalarınızda Saka Era takvim ayarlarını kolayca yönetmek ve gelişmiş tarih yönetimi için FieldCreateDate UseSakaEraCalendar özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldcreatedate/usesakaeracalendar/
---
## FieldCreateDate.UseSakaEraCalendar property

Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Örnekler

Belgenin oluşturulma tarihini/saatini görüntülemek için CREATEDATE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was created:");

// Belgenin oluşturulma tarihini ve saatini görüntülemek için CREATEDATE alanını kullanabiliriz.
// Aşağıda CREATEDATE alanının tarih/saati görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 - Hicri Takvim:
builder.Write("According to the Lunar Calendar - ");
FieldCreateDate field = (FieldCreateDate)builder.InsertField(FieldType.FieldCreateDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" CREATEDATE  \\h", field.GetFieldCode());

// 2 - Ümmü'l-Kurâ takvimi:
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
