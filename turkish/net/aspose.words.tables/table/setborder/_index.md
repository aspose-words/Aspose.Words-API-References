---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: .NET için Aspose.Words
description: SetBorder yöntemiyle tablonuzun görünümünü özelleştirin; profesyonel bir görünüm için çizgi stilini, genişliğini ve rengini ayarlayın. Tasarımınızı bugün geliştirin!
type: docs
weight: 430
url: /tr/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğe ve renge ayarlar.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| borderType | BorderType | Değiştirilecek tablo kenarlığı. |
| lineStyle | LineStyle | Uygulanacak çizgi stili. |
| lineWidth | Double | Ayarlanacak çizgi genişliği (puan cinsinden). |
| color | Color | Kenarlık için kullanılacak renk. |
| isOverrideCellBorders | Boolean | Ne zaman`doğru`, mevcut tüm açık hücre kenarlıklarının kaldırılmasına neden olur. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
