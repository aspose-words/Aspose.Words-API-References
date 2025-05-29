---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: .NET için Aspose.Words
description: ParagraphFormat LeftIndent özelliğiyle paragraflarınızın sol girintisini zahmetsizce ayarlayın. Daha iyi okunabilirlik için metin düzeninizi özelleştirin!
type: docs
weight: 180
url: /tr/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Paragraf için sol girintiyi temsil eden değeri (nokta cinsinden) alır veya ayarlar.

```csharp
public double LeftIndent { get; set; }
```

## Örnekler

Paragraf biçimlendirmesinin, merkezden uzak metin oluşturacak şekilde nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun yazdığı tüm metni ortala ve girintileri ayarla.
// Aşağıdaki girinti yapılandırması, sayfada asimetrik olarak yer alacak bir metin gövdesi oluşturacaktır.
// Metni hizalayacağımız "orta", sayfanın ortası değil, metnin gövdesinin ortası olacaktır.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
