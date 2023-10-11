---
title: Enum ImageType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.ImageType enum. Specifica il tipo formato di unimmagine in un documento Microsoft Word.
type: docs
weight: 1080
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
| NoImage | `0` | Non ci sono dati immagine. |
| Unknown | `1` | Un tipo di immagine sconosciuto o un tipo di immagine che non può essere archiviato direttamente in un documento Microsoft Word. |
| Emf | `2` | Metafile avanzato di Windows. |
| Wmf | `3` | Metafile di Windows. |
| Pict | `4` | Macintosh IMMAGINE. Un'immagine esistente verrà conservata in un documento, ma l'inserimento di nuove immagini PICT in un documento non è supportato. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Grafica di rete portatile. |
| Bmp | `7` | Bitmap di Windows. |
| Eps | `8` | PostScript incapsulato. |

### Esempi

Mostra come aggiungere un'immagine a una forma e controllarne il tipo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // L'immagine nell'URL è un file .gif. Inserendolo in un documento lo converte in un file .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Guarda anche

* property [ImageType](../imagedata/imagetype/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)


