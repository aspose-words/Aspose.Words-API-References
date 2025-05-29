---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.ImageType per gestire facilmente i formati immagine nei documenti di Microsoft Word. Migliora l'aspetto visivo del tuo documento!
type: docs
weight: 1410
url: /it/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Specifica il tipo (formato) di un'immagine in un documento Microsoft Word.

```csharp
public enum ImageType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| NoImage | `0` | Non ci sono dati di immagine. |
| Unknown | `1` | Un tipo di immagine sconosciuto o un tipo di immagine che non può essere memorizzato direttamente all'interno di un documento di Microsoft Word. |
| Emf | `2` | Metafile avanzato di Windows. |
| Wmf | `3` | Metafile di Windows. |
| Pict | `4` | Macintosh PICT. Un'immagine esistente verrà conservata in un documento, ma l'inserimento di nuove immagini PICT in un documento non è supportato. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Grafica di rete portatile. |
| Bmp | `7` | Bitmap di Windows. |
| Eps | `8` | PostScript incapsulato. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Esempi

Mostra come leggere un'immagine WebP.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Mostra come aggiungere un'immagine a una forma e verificarne il tipo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Guarda anche

* property [ImageType](../imagedata/imagetype/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
