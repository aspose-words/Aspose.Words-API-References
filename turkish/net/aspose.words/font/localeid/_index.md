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

Yerel ayar tanımlayıcılarının listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Örnekler

Bir belge oluşturucu ile eklediğimiz metnin yerel ayarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipinin yerel ayarını İngilizce olarak ayarlarsak ve biraz Rusça metin eklersek,
// İngilizce yerel yazım denetleyicisi metni tanımaz ve bir yazım hatası olarak algılar.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Uygun yazım denetleyicisini uygulamak üzere eklemek üzere olduğumuz metin için eşleşen bir yerel ayar belirleyin.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


