---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: .NET için Aspose.Words
description: Yerleşik stiller için yerel ayarlardan bağımsız StyleIdentifier özelliğini keşfedin. Projelerinizi tutarlı ve çok yönlü stil çözümleriyle geliştirin.
type: docs
weight: 180
url: /tr/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Yerleşik bir stil için yerel bağımsız stil tanımlayıcısını alır.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Notlar

Kullanıcı tanımlı (özel) stiller için bu özellik şunu döndürür:User.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
