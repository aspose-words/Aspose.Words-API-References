---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words for .NET
description: Font NameFarEast mülk. Doğu Asya yazı tipi adını döndürür veya ayarlar C#'da.
type: docs
weight: 260
url: /tr/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Doğu Asya yazı tipi adını döndürür veya ayarlar.

```csharp
public string NameFarEast { get; set; }
```

## Örnekler

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

* property [Name](../name/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
