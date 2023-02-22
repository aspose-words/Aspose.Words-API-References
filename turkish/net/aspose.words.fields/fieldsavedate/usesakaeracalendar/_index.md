---
title: FieldSaveDate.UseSakaEraCalendar
second_title: Aspose.Words for .NET API Referansı
description: FieldSaveDate mülk. Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldsavedate/usesakaeracalendar/
---
## FieldSaveDate.UseSakaEraCalendar property

Saka Dönemi takviminin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseSakaEraCalendar { get; set; }
```

### Örnekler

Belgenin Microsoft Word kullanılarak gerçekleştirilen en son kaydetme işleminin tarihini/saatini görüntülemek için KAYDET alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// KAYDET alanını belge üzerinde son kaydetme işleminin tarih ve saatini görüntülemek için kullanabiliriz.
// Bu alanların atıfta bulunduğu kaydetme işlemi, Microsoft Word gibi bir uygulamada manuel kaydetme işlemidir,
// belgenin Kaydet yöntemi değil.
// KAYDET alanının tarih/saati gösterebileceği üç farklı takvim türü aşağıdadır.
// 1 - İslami Ay Takvimi:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Ümmü'l-Kura takvimi:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Hindistan Ulusal takvimi:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE alanları, tarih/saat değerlerini yerleşik LastSavedTime özelliğinden alır.
// Belgenin Kaydetme yöntemi bu değeri güncellemeyecek, ancak yine de manuel olarak güncelleyebiliriz.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ayrıca bakınız

* class [FieldSaveDate](../)
* ad alanı [Aspose.Words.Fields](../../fieldsavedate/)
* toplantı [Aspose.Words](../../../)


