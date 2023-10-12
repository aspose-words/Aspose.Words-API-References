---
title: Font.LocaleId
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Biçimlendirilmiş karakterlerin yerel ayar tanımlayıcısını dili alır veya ayarlar.
type: docs
weight: 200
url: /tr/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Biçimlendirilmiş karakterlerin yerel ayar tanımlayıcısını (dili) alır veya ayarlar.

```csharp
public int LocaleId { get; set; }
```

### Notlar

Yerel tanımlayıcıların listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Örnekler

Belge oluşturucuyla eklediğimiz metnin yerel ayarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fontun yerel ayarını İngilizce olarak ayarlayıp bir miktar Rusça metin eklersek,
// İngilizce yerel yazım denetleyicisi metni tanımayacak ve onu bir yazım hatası olarak algılamayacaktır.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Eklemek üzere olduğumuz metin için uygun yazım denetleyiciyi uygulamak üzere eşleşen bir yerel ayar belirleyin.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


