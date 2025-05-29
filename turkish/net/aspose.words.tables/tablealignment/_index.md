---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: .NET için Aspose.Words
description: En iyi satır içi tablo hizalaması için Aspose.Words.Tables.TableAlignment enum'unu keşfedin. Belge biçimlendirmenizi hassasiyet ve kolaylıkla geliştirin.
type: docs
weight: 7200
url: /tr/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Satır içi bir tablo için hizalamayı belirtir.

```csharp
public enum TableAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Left | `0` | Tablo sola hizalanmıştır. |
| Center | `1` | Tablo ortalanmış. |
| Right | `2` | Tablo sağa hizalanmıştır. |

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

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
