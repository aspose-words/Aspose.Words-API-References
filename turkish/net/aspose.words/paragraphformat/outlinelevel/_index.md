---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words for .NET
description: ParagraphFormat OutlineLevel mülk. Belgedeki paragrafın anahat düzeyini belirtir C#'da.
type: docs
weight: 250
url: /tr/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Belgedeki paragrafın anahat düzeyini belirtir.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Örnekler

Daraltılabilir metin oluşturmak için paragraf anahat düzeylerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafta 1'den 9'a kadar herhangi bir sayı olabilen veya varsayılan "BodyText" değerinde bir OutlineLevel bulunur.
// Özelliği numaralı değerlerden birine ayarlamak solda bir ok gösterecektir
//paragrafın başlangıcı.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Seviye 1 en üst seviyedir. Daha yüksek düzeydeki bir paragrafın altında daha düşük düzeyde bir paragraf varsa,
// üst düzey paragrafın daraltılması, alt düzey paragrafın da daraltılmasına neden olacaktır.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Aynı seviyedeki iki paragraf birbirini daraltmayacak,
// ve oklar işaret ettikleri paragrafları daraltmaz.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Varsayılan "GövdeText" değeri, herhangi bir seviyedeki bir paragrafın daraltabileceği en düşük değerdir.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ayrıca bakınız

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
