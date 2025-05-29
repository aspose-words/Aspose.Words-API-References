---
title: FieldDate.UseLastFormat
linktitle: UseLastFormat
articleTitle: UseLastFormat
second_title: .NET için Aspose.Words
description: FieldDate UseLastFormat özelliğinin, uygulamalarınızda kusursuz entegrasyon için son kullanılan tarih biçimini koruyarak iş akışınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fielddate/uselastformat/
---
## FieldDate.UseLastFormat property

Yeni bir TARİH alanı eklerken barındırma uygulaması tarafından en son kullanılan biçimin kullanılıp kullanılmayacağını alır veya ayarlar.

```csharp
public bool UseLastFormat { get; set; }
```

## Örnekler

Farklı takvim türlerine göre tarihleri görüntülemek için DATE alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki metnin her zaman doğru tarihi göstermesini istiyorsak DATE alanını kullanabiliriz.
// Aşağıda, bir DATE alanının bir tarihi görüntülemek için kullanabileceği üç tür kültürel takvim bulunmaktadır.
// 1 - Hicri Takvim:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Ümmü'l-Kurâ takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Hindistan Ulusal Takvimi:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Bir TARİH alanı ekleyin ve takvim türünü, ana bilgisayar uygulaması tarafından en son kullanılan türe ayarlayın.
// Microsoft Word'de, tür Ekle -> Metin -> Tarih ve Saat iletişim kutusunda en son kullanılan tür olacaktır.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ayrıca bakınız

* class [FieldDate](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
