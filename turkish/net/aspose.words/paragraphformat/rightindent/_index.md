---
title: ParagraphFormat.RightIndent
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Paragraf için doğru girintiyi temsil eden değeri puan olarak alır veya ayarlar.
type: docs
weight: 260
url: /tr/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Paragraf için doğru girintiyi temsil eden değeri (puan olarak) alır veya ayarlar.

```csharp
public double RightIndent { get; set; }
```

### Örnekler

Merkez dışı metin oluşturmak için paragraf biçimlendirmesinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belge oluşturucunun yazdığı tüm metni ortalayın ve girintileri ayarlayın.
// Aşağıdaki girinti yapılandırması, sayfada asimetrik olarak oturacak bir metin gövdesi oluşturacaktır.
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
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


