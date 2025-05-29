---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Gelişmiş düzen kontrolü için belgenizin bölümündeki sütun sayısına kolayca erişmek amacıyla TextColumnCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

Bir belgenin bölümündeki sütun sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Bir bölümde birden fazla eşit aralıklı sütunun nasıl oluşturulacağını gösterir.

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

* class [TextColumnCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
