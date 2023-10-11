---
title: HtmlSaveOptions.ScaleImageToShapeSize
second_title: Aspose.Words per .NET API Reference
description: HtmlSaveOptions proprietà. Specifica se le immagini vengono ridimensionate da Aspose.Words alla dimensione della forma delimitante durante lesportazione in HTML MHTML o EPUB. Il valore predefinito èVERO .
type: docs
weight: 450
url: /it/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Specifica se le immagini vengono ridimensionate da Aspose.Words alla dimensione della forma delimitante durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`VERO` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

### Osservazioni

Un'immagine in un documento di Microsoft Word è una forma. La forma ha una dimensione e l'immagine ha una propria dimensione. Le dimensioni non sono direttamente collegate. Ad esempio, l'immagine può essere 1024x786 pixel, ma la forma che visualizza questa immagine può essere 400x300 punti.

Per poter visualizzare un'immagine nel browser, è necessario ridimensionarla in base alle dimensioni della forma. Il`ScaleImageToShapeSize` la proprietà controlla dove avviene il ridimensionamento di image : in Aspose.Words durante l'esportazione in HTML o nel browser durante la visualizzazione del documento.

Quando`ScaleImageToShapeSize` È`VERO` , l'immagine viene ridimensionata da Aspose.Words utilizzando il ridimensionamento di alta qualità durante l'esportazione in HTML. Quando`ScaleImageToShapeSize` è`falso`, l'immagine viene riprodotta con le sue dimensioni originali e il browser deve ridimensionarla.

In generale, i browser eseguono un ridimensionamento rapido e di scarsa qualità. Di conseguenza, normalmente otterrai una qualità di visualizzazione migliore nel browser e dimensioni del file più piccole quando`ScaleImageToShapeSize` È`VERO` , ma migliore qualità di stampa e conversione più rapida quando`ScaleImageToShapeSize` È`falso`.

Oltre alle forme contenenti singole immagini raster, questa opzione influisce anche sulle forme di gruppo costituite da immagini raster. Se`ScaleImageToShapeSize` È`falso` e una forma di gruppo contiene immagini raster la cui risoluzione intrinseca è superiore al valore specificato in[`ImageResolution`](../imageresolution/), Aspose.Words aumenterà la risoluzione di rendering per quel gruppo. Ciò consente di preservare meglio la qualità delle immagini raggruppate ad alta risoluzione durante il salvataggio in HTML.

### Esempi

Mostra come disabilitare il ridimensionamento delle immagini rispetto alle dimensioni della forma principale durante il salvataggio in .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Inserisci una forma che contiene un'immagine, quindi rendi quella forma considerevolmente più piccola dell'immagine.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // Il salvataggio di un documento che contiene forme con immagini in HTML creerà un file immagine nel file system locale
            // per ciascuna di queste forme. Il documento HTML di output utilizzerà <image> tag per collegare e visualizzare queste immagini.
            // Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per determinare
            // se ridimensionare tutte le immagini che si trovano all'interno delle forme alle dimensioni delle rispettive forme.
            // Impostando il flag "ScaleImageToShapeSize" su "true" rimpicciolirà ogni immagine
            // alla dimensione della forma che la contiene, in modo che nessuna immagine salvata sia più grande di quanto richiesto dal documento.
            // Impostando il flag "ScaleImageToShapeSize" su "false" si manterranno le dimensioni originali di queste immagini,
            // che occuperà più spazio in cambio della preservazione della qualità dell'immagine.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Guarda anche

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../htmlsaveoptions/)
* assemblea [Aspose.Words](../../../)


