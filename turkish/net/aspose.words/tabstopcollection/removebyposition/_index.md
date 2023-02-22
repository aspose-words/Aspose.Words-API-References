---
title: TabStopCollection.RemoveByPosition
second_title: Aspose.Words for .NET API Referansı
description: TabStopCollection yöntem. Belirtilen konumdaki bir sekme durağını koleksiyondan kaldırır.
type: docs
weight: 120
url: /tr/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Belirtilen konumdaki bir sekme durağını koleksiyondan kaldırır.

```csharp
public void RemoveByPosition(double position)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| position | Double | Sekmenin konumu (nokta olarak) kaldırılacak duraktır. |

### Örnekler

TOC ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// İçindekiler sonuç tabanlı stiller ile tüm paragrafları yineleyin; Bu, TOC ve TOC9 arasındaki herhangi bir stildir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi alın, bu, sayfa numaralarını hizalamak için kullanılan sekme olmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekmeyi değiştirin, özel bir sekme durağı ile durdurun.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* class [TabStopCollection](../)
* ad alanı [Aspose.Words](../../tabstopcollection/)
* toplantı [Aspose.Words](../../../)


