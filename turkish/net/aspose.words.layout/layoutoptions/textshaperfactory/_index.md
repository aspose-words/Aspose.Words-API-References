---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: .NET için Aspose.Words
description: Gelişmiş tipografi için LayoutOptions TextShaperFactory özelliğini keşfedin. Özelleştirilebilir ITextShaperFactory uygulamalarıyla işlemelerinizi geliştirin.
type: docs
weight: 100
url: /tr/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Alır veya ayarlar[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) Gelişmiş Tipografi oluşturma özellikleri için kullanılan uygulama.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Örnekler

HarfBuzz metin şekillendirme motorunu kullanarak OpenType özelliklerinin nasıl destekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words harici olarak sağlanan metin şekillendirici nesnelerini kullanabilir,
// yazı tiplerini temsil eder ve metin için şekillendirme bilgilerini hesaplar.
// Birden fazla yazı tipi kullanan belgeler için bir metin şekillendirici fabrikası gereklidir.
// Metin şekillendirici fabrika ayarlarına getirildiğinde, düzen OpenType özelliklerini kullanır.
// Bir Instance özelliği, HarfBuzzTextShaperFactory'yi sarmalayan statik bir BasicTextShaperCache nesnesi döndürür.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Şu anda PDF veya XPS formatlarına aktarım sırasında metin şekillendirme gerçekleştiriliyor.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Ayrıca bakınız

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
