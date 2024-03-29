---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Tables.TableAlignment Sıralama. Satır içi tablo için hizalamayı belirtir C#'da.
type: docs
weight: 6350
url: /tr/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Satır içi tablo için hizalamayı belirtir.

```csharp
public enum TableAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Tablo sola hizalanmıştır. |
| Center | `1` | Tablo ortalanmıştır. |
| Right | `2` | Tablo sağa hizalanmıştır. |

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

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
