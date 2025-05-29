---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: .NET için Aspose.Words
description: TextColumnCollection SetCount yöntemiyle düzeninizi optimize edin; metni istediğiniz sütun sayısına zahmetsizce yerleştirerek okunabilirliği artırın.
type: docs
weight: 70
url: /tr/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Metni belirtilen sayıda metin sütununa düzenler.

```csharp
public void SetCount(int newCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newCount | Int32 | Metnin kaç sütuna yerleştirileceği. |

## Notlar

Ne zaman[`EvenlySpaced`](../evenlyspaced/) dır`YANLIŞ` ve sütun sayısını artırırsanız, yeni[`TextColumn`](../../textcolumn/) nesneler sıfır genişlik ve aralıkla oluşturulur. Yeni sütunlar için genişlik ve aralık ayarlamanız gerekir.

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
