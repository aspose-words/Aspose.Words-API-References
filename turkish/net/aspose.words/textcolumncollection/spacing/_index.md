---
title: TextColumnCollection.Spacing
second_title: Aspose.Words for .NET API Referansı
description: TextColumnCollection mülk. Sütunlar eşit aralıklarla yerleştirildiğinde her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Sütunlar eşit aralıklarla yerleştirildiğinde, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar.

```csharp
public double Spacing { get; set; }
```

### Notlar

Yalnızca şu durumlarda etkili olur:[`EvenlySpaced`](../evenlyspaced/) ayarlandı`doğru` .

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


