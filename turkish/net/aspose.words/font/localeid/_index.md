---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: .NET için Aspose.Words
description: Font LocaleId özelliğinin çeşitli karakter dilleri için yerel tanımlayıcıları yöneterek metin biçimlendirmenizi nasıl geliştirdiğini keşfedin. Kodlamanızı bugün geliştirin!
type: docs
weight: 200
url: /tr/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Biçimlendirilmiş karakterlerin yerel tanımlayıcısını (dil) alır veya ayarlar.

```csharp
public int LocaleId { get; set; }
```

## Notlar

Yerel tanımlayıcıların listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Örnekler

Belge oluşturucu ile eklediğimiz metnin yerel ayarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipinin yerel ayarını İngilizce olarak ayarlayıp biraz Rusça metin eklersek,
// İngilizce yerel yazım denetleyicisi metni tanımayacak ve bunu bir yazım hatası olarak algılayacaktır.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Eklemek üzere olduğumuz metne uygun yazım denetimini uygulamak için eşleşen bir yerel ayar belirleyin.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
