---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: Aspose.Words for .NET
description: ParagraphFormat TabStops mülk. Bu nesne için tanımlanan özel sekme duraklarının koleksiyonunu alır C#'da.
type: docs
weight: 390
url: /tr/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Bu nesne için tanımlanan özel sekme duraklarının koleksiyonunu alır.

```csharp
public TabStopCollection TabStops { get; }
```

## Örnekler

İçindekiler ile ilgili paragraflarda sağ sekme durağının konumunun nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// İçindekiler sonuç tabanlı stillerle tüm paragrafları yineleyin; bu, TOC ve TOC9 arasındaki herhangi bir stildir.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Bu paragrafta kullanılan ilk sekmeyi alın, bu sayfa numaralarını hizalamak için kullanılan sekme olmalıdır.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // İlk varsayılan sekmeyi değiştirin, özel bir sekme durağıyla durdurun.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Ayrıca bakınız

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
