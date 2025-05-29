---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: TabStop Position özelliğini keşfederek noktalardaki sekme durağı konumlarını kolayca bulabilir, düzen hassasiyetinizi ve tasarım verimliliğinizi artırabilirsiniz.
type: docs
weight: 50
url: /tr/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Sekme durağının konumunu noktalar halinde alır.

```csharp
public double Position { get; }
```

## Örnekler

İçindekiler ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// TOC sonuç tabanlı stillerle tüm paragraflarda gezinin; bu, TOC ile TOC9 arasındaki herhangi bir stil olabilir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi al, bu sekme sayfa numaralarını hizalamak için kullanılmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekme durağını özel bir sekme durağıyla değiştir.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* class [TabStop](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
