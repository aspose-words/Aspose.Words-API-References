---
title: AutoFitBehavior Enum
linktitle: AutoFitBehavior
articleTitle: AutoFitBehavior
second_title: .NET için Aspose.Words
description: AutoFit yöntemiyle tablo yeniden boyutlandırmayı optimize etmek, belge düzenini ve sunumunu geliştirmek için Aspose.Words.Tables.AutoFitBehavior enum'unu keşfedin.
type: docs
weight: 7080
url: /tr/net/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enumeration

Aspose.Words'ün tabloyu nasıl yeniden boyutlandıracağını belirler.[`AutoFit`](../table/autofit/) yöntem.

```csharp
public enum AutoFitBehavior
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| AutoFitToContents | `0` | Aspose.Words, Otomatik Sığdır seçeneğini etkinleştirir, tablodan ve tüm hücrelerden tercih edilen genişliği kaldırır ve ardından tablo düzenini günceller. |
| AutoFitToWindow | `1` | Bu değeri kullandığınızda, Aspose.Words Otomatik Sığdır seçeneğini etkinleştirir, tablo için tercih edilen genişliği %100 olarak ayarlar, tercih edilen genişlikleri tüm hücrelerden kaldırır ve ardından tablo düzenini günceller. |
| FixedColumnWidths | `2` | Aspose.Words, AutoFit seçeneğini devre dışı bırakır ve tercih edileni tablodan kaldırır. |

## Örnekler

Bir stil uygulanırken yeni bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Herhangi bir tablo biçimlendirmesini ayarlamadan önce en az bir satır eklemeliyiz.
builder.InsertCell();

// Stil tanımlayıcısına göre kullanılan tablo stilini ayarlayın.
// .doc formatına kaydederken tüm tablo stillerinin kullanılamayacağını unutmayın.
table.StyleIdentifier = StyleIdentifier.MediumShading1Accent1;

// Tablonun özelliklerine tahminlere dayalı olarak stili kısmen uygulayın, ardından tabloyu oluşturun.
table.StyleOptions =
    TableStyleOptions.FirstColumn | TableStyleOptions.RowBands | TableStyleOptions.FirstRow;
table.AutoFit(AutoFitBehavior.AutoFitToContents);

builder.Writeln("Item");
builder.CellFormat.RightPadding = 40;
builder.InsertCell();
builder.Writeln("Quantity (kg)");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Apples");
builder.InsertCell();
builder.Writeln("20");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Bananas");
builder.InsertCell();
builder.Writeln("40");
builder.EndRow();

builder.InsertCell();
builder.Writeln("Carrots");
builder.InsertCell();
builder.Writeln("50");
builder.EndRow();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithStyle.docx");
```

Biçimlendirilmiş 2x2'lik bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Tablo oluşturulurken, belge oluşturucu geçerli RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecin bulunduğu geçerli satıra/hücreye ve bunları oluştururken oluşacak yeni satırlara/hücrelere.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Daha önce eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesinde yapılan değişikliklerden geriye dönük olarak etkilenmez.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
