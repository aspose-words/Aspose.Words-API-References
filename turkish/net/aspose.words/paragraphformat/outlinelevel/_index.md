---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: .NET için Aspose.Words
description: Belgelerinizdeki paragraf hiyerarşisini kolayca tanımlamak, organizasyonu ve okunabilirliği artırmak için ParagraphFormat OutlineLevel özelliğini keşfedin.
type: docs
weight: 260
url: /tr/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Belgedeki paragrafın ana hat düzeyini belirtir.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Örnekler

Daraltılabilir metin oluşturmak için paragraf anahat düzeylerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Her paragrafın bir OutlineLevel değeri vardır. Bu değer 1 ile 9 arasında herhangi bir sayı veya varsayılan "BodyText" değeri olabilir.
// Özelliği numaralandırılmış değerlerden birine ayarlamak sola doğru bir ok gösterecektir
// paragrafın başlangıcı.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Seviye 1 en üst seviyedir. Daha yüksek seviyedeki bir paragrafın altında daha düşük seviyedeki bir paragraf varsa,
// üst düzey paragrafı daraltmak alt düzey paragrafı da daraltacaktır.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Aynı seviyedeki iki paragraf birbirini daraltmaz,
// ve oklar işaret ettikleri paragrafları daraltmaz.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Varsayılan "BodyText" değeri, herhangi bir düzeydeki bir paragrafın daraltabileceği en düşük değerdir.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Ayrıca bakınız

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
