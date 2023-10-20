---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words for .NET
description: TextColumnCollection SetCount yöntem. Metni belirtilen sayıda metin sütunu halinde düzenler C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Metni belirtilen sayıda metin sütunu halinde düzenler.

```csharp
public void SetCount(int newCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newCount | Int32 | Metnin düzenleneceği sütun sayısı. |

## Notlar

Ne zaman[`EvenlySpaced`](../evenlyspaced/) dır-dir`YANLIŞ` ve sütun sayısını artırırsınız, new[`TextColumn`](../../textcolumn/) nesneler sıfır genişlik ve aralıkla oluşturulur. Yeni sütunlar için genişlik ve aralık ayarlamanız gerekir.

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

* class [TextColumnCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
