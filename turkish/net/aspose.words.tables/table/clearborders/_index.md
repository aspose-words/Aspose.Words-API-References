---
title: Table.ClearBorders
linktitle: ClearBorders
articleTitle: ClearBorders
second_title: .NET için Aspose.Words
description: Tasarımınızın netliğini ve çekiciliğini artırarak tüm tablo ve hücre kenarlıklarını zahmetsizce ortadan kaldırmak için Table ClearBorders yöntemini keşfedin.
type: docs
weight: 390
url: /tr/net/aspose.words.tables/table/clearborders/
---
## Table.ClearBorders method

Bu tablodaki tüm tablo ve hücre kenarlıklarını kaldırır.

```csharp
public void ClearBorders()
```

## Örnekler

Bir tabloya dış kenarlığın nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tabloyu sayfanın ortasına hizala.
table.Alignment = TableAlignment.Center;

// Tablodaki mevcut tüm kenarlıkları ve gölgelendirmeleri temizleyin.
table.ClearBorders();
table.ClearShading();

// Tablonun dış hatlarına yeşil kenarlıklar ekleyin.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Hücreleri açık yeşil düz bir renkle doldurun.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

Bir tablodan tüm kenarlıkların nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

// Üst sınırın rengini ve kalınlığını değiştirin.
Border topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];
table.SetBorder(BorderType.Top, LineStyle.Double, 1.5, Color.Red, true);

Assert.AreEqual(1.5d, topBorder.LineWidth);
Assert.AreEqual(Color.Red.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.Double, topBorder.LineStyle);

// Tablodaki tüm hücrelerin sınırlarını temizleyin ve ardından belgeyi kaydedin.
table.ClearBorders();
doc.Save(ArtifactsDir + "Table.ClearBorders.docx");

// Belgeyi tekrar açtıktan sonra tablonun özelliklerinin değerlerini doğrulayın.
doc = new Document(ArtifactsDir + "Table.ClearBorders.docx");
table = doc.FirstSection.Body.Tables[0];
topBorder = table.FirstRow.RowFormat.Borders[BorderType.Top];

Assert.AreEqual(0.0d, topBorder.LineWidth);
Assert.AreEqual(Color.Empty.ToArgb(), topBorder.Color.ToArgb());
Assert.AreEqual(LineStyle.None, topBorder.LineStyle);
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
