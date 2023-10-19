---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.TextWrapping Sıralama. Metnin tablonun etrafına nasıl sarılacağını belirtir C#'da.
type: docs
weight: 6380
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
| None | `0` | Metin ve tablo, belgedeki görünüm sırasına göre görüntülenir. |
| Around | `1` | Metin masanın çevresine sarılarak yan taraftaki boş alanı kaplar. |
| Default | `0` | Varsayılan değer. |

## Örnekler

Tablo metni kaydırmayla nasıl çalışılacağını gösterir.

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

// Tablonun etrafındaki metni sarmasını sağlamak için "TextWrapping" özelliğini "TextWrapping.Around" olarak ayarlayın,
// ve konumu ayarlayarak aşağıdaki paragrafın içine doğru itin.
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
