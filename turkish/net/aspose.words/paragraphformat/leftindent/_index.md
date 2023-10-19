---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words for .NET
description: ParagraphFormat LeftIndent mülk. Paragrafın sol girintisini temsil eden değeri puan cinsinden alır veya ayarlar C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

Paragrafın sol girintisini temsil eden değeri (puan cinsinden) alır veya ayarlar.

```csharp
public double LeftIndent { get; set; }
```

## Örnekler

Merkezin dışında metin oluşturmak için paragraf formatının nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun yazdığı tüm metni ortalayın ve girintileri ayarlayın.
// Aşağıdaki girinti yapılandırması sayfada asimetrik olarak oturacak bir metin gövdesi oluşturacaktır.
// Metni hizaladığımız "merkez", sayfanın ortası değil, metnin gövdesinin ortası olacaktır.
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
