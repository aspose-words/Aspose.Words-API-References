---
title: FieldDate.UseLastFormat
second_title: Aspose.Words for .NET API Referansı
description: FieldDate mülk. Yeni bir DATE alanı eklenirken barındırma uygulaması tarafından en son kullanılan biçimin kullanılıp kullanılmayacağını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Yeni bir DATE alanı eklenirken barındırma uygulaması tarafından en son kullanılan biçimin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseLastFormat { get; set; }
```

### Örnekler

Farklı takvim türlerine göre tarihleri görüntülemek için TARİH alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki metnin her zaman doğru tarihi göstermesini istiyorsak DATE alanını kullanabiliriz.
// Aşağıda DATE alanının tarihi görüntülemek için kullanabileceği üç tür kültürel takvim bulunmaktadır.
// 1 - İslami Ay Takvimi:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Ümmü'l-Kura takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Hindistan Ulusal Takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Bir DATE alanı ekleyin ve takvim türünü, ana bilgisayar uygulamasının en son kullandığına ayarlayın.
// Microsoft Word'de, tür Ekle'de en son kullanılan tür olacaktır -> Metin -> Tarih ve Saat iletişim kutusu.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ayrıca bakınız

* class [FieldDate](../)
* ad alanı [Aspose.Words.Fields](../../fielddate/)
* toplantı [Aspose.Words](../../../)


