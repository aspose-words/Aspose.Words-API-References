---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words for .NET
description: PageSetup TextColumns mülk. Metin sütunları kümesini temsil eden bir koleksiyon döndürür C#'da.
type: docs
weight: 420
url: /tr/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

Metin sütunları kümesini temsil eden bir koleksiyon döndürür.

```csharp
public TextColumnCollection TextColumns { get; }
```

## Örnekler

Bir bölümde birden çok eşit aralıklı sütunun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Ayrıca bakınız

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
