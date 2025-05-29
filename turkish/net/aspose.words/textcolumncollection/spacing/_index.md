---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: .NET için Aspose.Words
description: TextColumnCollection Spacing özelliğini keşfedin, cilalı, profesyonel bir düzen için sütun aralıklarını noktalar halinde zahmetsizce yönetin. Tasarımınızı bugün geliştirin!
type: docs
weight: 50
url: /tr/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

Sütunlar eşit aralıklı olduğunda, her sütun arasındaki boşluk miktarını noktalar halinde alır veya ayarlar.

```csharp
public double Spacing { get; set; }
```

## Notlar

Yalnızca şu durumlarda etkilidir:[`EvenlySpaced`](../evenlyspaced/) ayarlandı`doğru` .

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
