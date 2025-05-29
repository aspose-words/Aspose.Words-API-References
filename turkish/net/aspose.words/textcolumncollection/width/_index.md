---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: .NET için Aspose.Words
description: TextColumnCollection Width özelliğini keşfedin. Projelerinizde optimum düzen ve tasarım için eşit aralıklı sütunları kolayca yönetin.
type: docs
weight: 60
url: /tr/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

Sütunlar eşit aralıklı olduğunda sütunların genişliğini alır.

```csharp
public double Width { get; }
```

## Notlar

Yalnızca şu durumlarda etkilidir:[`EvenlySpaced`](../evenlyspaced/) ayarlandı`doğru`.

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
