---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: .NET için Aspose.Words
description: Özel sekme duraklarını kolayca yönetmek, belge biçimlendirmenizi geliştirmek ve okunabilirliği artırmak için ParagraphFormat TabStops özelliğini keşfedin.
type: docs
weight: 400
url: /tr/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Bu nesne için tanımlanmış özel sekme duraklarının koleksiyonunu alır.

```csharp
public TabStopCollection TabStops { get; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
