---
title: TabStop.Alignment
second_title: Aspose.Words for .NET API Referansı
description: TabStop mülk. Bu sekme durağındaki metnin hizalamasını alır veya ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

Bu sekme durağındaki metnin hizalamasını alır veya ayarlar.

```csharp
public TabAlignment Alignment { get; set; }
```

### Örnekler

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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* ad alanı [Aspose.Words](../../tabstop/)
* toplantı [Aspose.Words](../../../)


