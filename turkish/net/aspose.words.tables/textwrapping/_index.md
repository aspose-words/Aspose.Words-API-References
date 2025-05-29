---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: .NET için Aspose.Words
description: Tabloların etrafında etkili metin sarma için Aspose.Words.Tables.TextWrapping enum'unu keşfedin. Belge biçimlendirmenizi kolaylıkla geliştirin!
type: docs
weight: 7230
url: /tr/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

Metnin tablonun etrafına nasıl sarılacağını belirtir.

```csharp
public enum TextWrapping
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Metin ve tablo, belgede göründükleri sıraya göre görüntülenir. |
| Around | `1` | Metin, tablonun etrafına sarılmış ve mevcut kenar alanını kaplıyor. |
| Default | `0` | Varsayılan değer. |

## Örnekler

Tablo metin kaydırmanın nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Tablonun metni etrafına sarmasını sağlamak için "TextWrapping" özelliğini "TextWrapping.Around" olarak ayarlayın,
// ve pozisyonunu ayarlayarak aşağıdaki paragrafa doğru itin.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
