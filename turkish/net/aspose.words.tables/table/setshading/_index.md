---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: .NET için Aspose.Words
description: SetShading yöntemiyle tablonuzun görünümünü geliştirin; cilalı, profesyonel bir görünüm için özel gölgelendirme değerleri uygulayın.
type: docs
weight: 450
url: /tr/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Tüm tabloda gölgelendirmeyi belirtilen değerlere ayarlar.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| texture | TextureIndex | Uygulanacak doku. |
| foregroundColor | Color | Dokunun rengi. |
| backgroundColor | Color | Arkaplan dolgusunun rengi. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
