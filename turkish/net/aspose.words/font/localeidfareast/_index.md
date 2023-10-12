---
title: Font.LocaleIdFarEast
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Biçimlendirilmiş Asya karakterlerinin yerel ayar tanımlayıcısını dili alır veya ayarlar.
type: docs
weight: 220
url: /tr/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Biçimlendirilmiş Asya karakterlerinin yerel ayar tanımlayıcısını (dili) alır veya ayarlar.

```csharp
public int LocaleIdFarEast { get; set; }
```

### Notlar

Yerel tanımlayıcıların listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

### Örnekler

Uzak Doğu dilinde metnin nasıl ekleneceğini ve biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun eklediği herhangi bir metne uygulayacağı yazı tipi ayarlarını belirtin.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Yazı tipimiz ve yerel ayarımızın "UzakDoğu" eşdeğerlerini adlandırın.
// Eğer oluşturucu bu Font konfigürasyonuna Asya karakterleri eklerse, aşağıdakileri içeren her çalıştırma
// bu karakterler, varsayılan yerine "FarEast" yazı tipi/yerel ayarı kullanılarak görüntülenecektir.
// Batı yazı tipinin Asya karakterleri için ideal temsilleri olmadığında bu yararlı olabilir.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Bu metin varsayılan yazı tipinde/yerel ayarda görüntülenecektir.
builder.Writeln("Hello world!");

// Bunlar Asya karakterleri olduğundan, bu çalıştırma "UzakDoğu" yazı tipi/yerel eşdeğerlerimizi uygulayacaktır.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


