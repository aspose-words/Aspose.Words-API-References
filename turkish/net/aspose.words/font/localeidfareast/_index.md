---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: .NET için Aspose.Words
description: Biçimlendirilmiş Asya karakterleri için yerel tanımlayıcıları kolayca yönetmek ve çok dilli uygulamalarınızı geliştirmek için Font LocaleIdFarEast özelliğini keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Biçimlendirilmiş Asya karakterlerinin yerel tanımlayıcısını (dil) alır veya ayarlar.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Notlar

Yerel tanımlayıcıların listesi için bkz. https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Örnekler

Uzak Doğu dillerinden birinde metnin nasıl ekleneceği ve biçimlendirileceği gösterilmektedir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun eklediği herhangi bir metne uygulayacağı yazı tipi ayarlarını belirtin.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Yazı tipimiz ve yerel ayarımız için "FarEast" eşdeğerlerini adlandırın.
// Oluşturucu bu Yazı Tipi yapılandırmasıyla Asya karakterleri eklerse, o zaman içeren her çalışma
// bu karakterler varsayılan yerine "FarEast" yazı tipi/yerel ayarını kullanarak görüntülenecektir.
// Bu, batılı bir yazı tipinin Asya karakterleri için ideal temsillere sahip olmadığı durumlarda yararlı olabilir.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Bu metin varsayılan yazı tipi/yerel ayarlarında gösterilecektir.
builder.Writeln("Hello world!");

// Bunlar Asya karakterleri olduğundan, bu çalıştırmada "UzakDoğu" yazı tipi/yerel eşdeğerlerimiz uygulanacaktır.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
