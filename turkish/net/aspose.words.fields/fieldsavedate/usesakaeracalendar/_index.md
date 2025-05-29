---
title: FieldSaveDate.UseSakaEraCalendar
linktitle: UseSakaEraCalendar
articleTitle: UseSakaEraCalendar
second_title: .NET için Aspose.Words
description: FieldSaveDate'in Saka Era Takvim özelliğiyle tarihleri zahmetsizce yönetin. Gelişmiş tarih takibi ve organizasyonu için ayarları kolayca değiştirin.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

## Örnekler

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini görüntülemek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Belgedeki son kaydetme işleminin tarih ve saatini görüntülemek için SAVEDATE alanını kullanabiliriz.
// Bu alanların atıfta bulunduğu kaydetme işlemi, Microsoft Word gibi bir uygulamada manuel kaydetmedir.
// belgenin Kaydetme yöntemi değil.
// Aşağıda SAVEDATE alanının tarih/saati görüntüleyebileceği üç farklı takvim türü bulunmaktadır.
// 1 - Hicri Takvim:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Ümmü'l-Kurâ takvimi:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Hindistan Ulusal Takvimi:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE alanları tarih/saat değerlerini LastSavedTime yerleşik özelliğinden alır.
// Belgenin Kaydetme metodu bu değeri güncellemeyecektir, ancak yine de manuel olarak güncelleyebiliriz.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ayrıca bakınız

* class [FieldSaveDate](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
