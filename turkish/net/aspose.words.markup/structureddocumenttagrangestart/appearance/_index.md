---
title: StructuredDocumentTagRangeStart.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi ve iyileştirilmiş okunabilirlik için StructuredDocumentTagRangeStart görünümünün nasıl özelleştirileceğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.markup/structureddocumenttagrangestart/appearance/
---
## StructuredDocumentTagRangeStart.Appearance property

Yapılandırılmış belge etiketinin görünümünü alır veya ayarlar.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Örnekler

İçeriğin etrafında etiketin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### Ayrıca bakınız

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTagRangeStart](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
