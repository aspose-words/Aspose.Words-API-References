---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: .NET için Aspose.Words
description: Microsoft Word belgelerindeki resim biçimlerini kolayca yönetmek için Aspose.Words.Drawing.ImageType enum'unu keşfedin. Belgenizin görsel çekiciliğini artırın!
type: docs
weight: 1410
url: /tr/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Microsoft Word belgesindeki bir görüntünün türünü (biçimini) belirtir.

```csharp
public enum ImageType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| NoImage | `0` | Görüntü verisi yok. |
| Unknown | `1` | Bilinmeyen bir görüntü türü veya doğrudan bir Microsoft Word belgesinin içine depolanamayan görüntü türü. |
| Emf | `2` | Windows Gelişmiş Meta Dosyası. |
| Wmf | `3` | Windows Meta Dosyası. |
| Pict | `4` | Macintosh PICT. Mevcut bir görüntü bir belgede korunacaktır, ancak bir belgeye yeni PICT görüntüleri eklemek desteklenmez. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Taşınabilir Ağ Grafikleri. |
| Bmp | `7` | Windows Bit Eşlemi. |
| Eps | `8` | Kapsüllenmiş PostScript. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Örnekler

WebP görüntüsünün nasıl okunacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Bir şekle nasıl resim ekleneceğini ve tipinin nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Ayrıca bakınız

* property [ImageType](../imagedata/imagetype/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
