---
title: Table.ClearShading
linktitle: ClearShading
articleTitle: ClearShading
second_title: .NET için Aspose.Words
description: Projelerinizde tablo gölgelendirmesini zahmetsizce ortadan kaldırmak, netliği ve sunumu geliştirmek için Tablo ClearShading yöntemini keşfedin.
type: docs
weight: 400
url: /tr/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

Tablodaki tüm gölgelendirmeyi kaldırır.

```csharp
public void ClearShading()
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

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
