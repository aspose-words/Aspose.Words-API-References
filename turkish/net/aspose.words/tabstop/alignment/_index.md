---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: .NET için Aspose.Words
description: Belgenizin düzenini ve okunabilirliğini artırarak sekme duraklarındaki metin hizalamasını kolayca özelleştirmek için TabStop Hizalama özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Bu sekme durağında metnin hizalamasını alır veya ayarlar.

```csharp
public TabAlignment Alignment { get; set; }
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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
