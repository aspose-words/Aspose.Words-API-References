---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words for .NET
description: Table SetBorder yöntem. Belirtilen tablo kenarlığını belirtilen çizgi stiline genişliğine ve rengine ayarlar C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğine ve rengine ayarlar.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| borderType | BorderType | Tablo kenarlığı değiştirilecek. |
| lineStyle | LineStyle | Uygulanacak çizgi stili. |
| lineWidth | Double | Ayarlanacak çizgi genişliği (nokta cinsinden). |
| color | Color | Kenarlık için kullanılacak renk. |
| isOverrideCellBorders | Boolean | Ne zaman`doğru`, mevcut tüm açık hücre sınırlarının kaldırılmasına neden olur. |

## Örnekler

Bir tabloya anahat kenarlığının nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Tabloyu sayfanın ortasına hizalayın.
table.Alignment = TableAlignment.Center;

// Tablodaki mevcut sınırları ve gölgeleri temizleyin.
table.ClearBorders();
table.ClearShading();

// Tablonun ana hatlarına yeşil kenarlıklar ekleyin.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Hücreleri açık yeşil düz renkle doldurun.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Ayrıca bakınız

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
