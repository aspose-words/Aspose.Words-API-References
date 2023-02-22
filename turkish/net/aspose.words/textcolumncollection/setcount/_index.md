---
title: TextColumnCollection.SetCount
second_title: Aspose.Words for .NET API Referansı
description: TextColumnCollection yöntem. Metni belirtilen sayıda metin sütununa göre düzenler.
type: docs
weight: 70
url: /tr/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

Metni belirtilen sayıda metin sütununa göre düzenler.

```csharp
public void SetCount(int newCount)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| newCount | Int32 | Metnin düzenleneceği sütun sayısı. |

### Notlar

Ne zaman[`EvenlySpaced`](../evenlyspaced/) dır-dir **yanlış** ve sütun sayısını artırırsınız, yeni[`TextColumn`](../../textcolumn/) nesneler sıfır genişlik ve boşluk ile oluşturulur. Yeni sütunlar için genişlik ve boşluk ayarlamanız gerekir.

### Örnekler

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
* ad alanı [Aspose.Words](../../textcolumncollection/)
* toplantı [Aspose.Words](../../../)


