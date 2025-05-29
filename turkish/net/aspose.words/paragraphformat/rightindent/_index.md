---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: .NET için Aspose.Words
description: ParagraphFormat RightIndent özelliğiyle paragraflarınızın sağ girintisini nasıl kolayca ayarlayabileceğinizi keşfedin. Belgenizin biçimlendirmesini bugün geliştirin!
type: docs
weight: 280
url: /tr/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Paragraf için sağ girintiyi temsil eden değeri (nokta cinsinden) alır veya ayarlar.

```csharp
public double RightIndent { get; set; }
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
