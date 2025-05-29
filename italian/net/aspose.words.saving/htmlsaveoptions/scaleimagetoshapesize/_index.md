---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ScaleImageToShapeSize di HtmlSaveOptions ottimizza il ridimensionamento delle immagini in Aspose.Words per l'esportazione in HTML, MHTML o EPUB. Migliora i tuoi documenti!
type: docs
weight: 470
url: /it/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Specifica se le immagini vengono ridimensionate da Aspose.Words in base alle dimensioni della forma di delimitazione durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`VERO` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Osservazioni

Un'immagine in un documento di Microsoft Word è una forma. La forma ha una dimensione e l'immagine ha le sue dimensioni. Le dimensioni non sono direttamente collegate. Ad esempio, l'immagine può essere 1024x786 pixel, , ma la forma che la visualizza può essere 400x300 punti.

Per visualizzare un'immagine nel browser, è necessario ridimensionarla in base alle dimensioni della forma. Il`ScaleImageToShapeSize` La proprietà controlla dove avviene il ridimensionamento dell'immagine image : in Aspose.Words durante l'esportazione in HTML o nel browser durante la visualizzazione del documento.

Quando`ScaleImageToShapeSize` È`VERO` , l'immagine viene ridimensionata da Aspose.Words utilizzando un ridimensionamento di alta qualità durante l'esportazione in HTML. Quando`ScaleImageToShapeSize` è`falso`, l'immagine viene visualizzata nelle sue dimensioni originali e il browser deve ridimensionarla.

In generale, i browser eseguono ridimensionamenti rapidi e di scarsa qualità. Di conseguenza, si ottiene normalmente una migliore qualità di visualizzazione nel browser e dimensioni del file inferiori quando`ScaleImageToShapeSize` È`VERO` , ma una migliore qualità di stampa e una conversione più rapida quando`ScaleImageToShapeSize` È`falso`.

Oltre alle forme contenenti singole immagini raster, questa opzione influisce anche sulle forme di gruppo costituite da immagini raster. Se`ScaleImageToShapeSize` È`falso` e una forma di gruppo contiene immagini raster la cui risoluzione intrinseca è superiore al valore specificato in[`ImageResolution`](../imageresolution/), Aspose.Words aumenterà la risoluzione di rendering per quel gruppo. Questo permette di preservare meglio la qualità delle immagini ad alta risoluzione raggruppate durante il salvataggio in HTML.

## Esempi

Mostra come disattivare il ridimensionamento delle immagini in base alle dimensioni della forma padre quando si salva in formato .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma che contiene un'immagine, quindi rendi la forma considerevolmente più piccola dell'immagine.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// Il salvataggio di un documento contenente forme con immagini in HTML creerà un file immagine nel file system locale
// per ciascuna di queste forme. Il documento HTML di output utilizzerà i tag <image> per collegarsi e visualizzare queste immagini.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions per determinare
// se ridimensionare tutte le immagini che si trovano all'interno di forme in base alle dimensioni delle loro forme.
// Impostando il flag "ScaleImageToShapeSize" su "true" ogni immagine verrà rimpicciolita
// alla dimensione della forma che la contiene, in modo che nessuna immagine salvata sia più grande di quanto richiesto dal documento.
// Impostando il flag "ScaleImageToShapeSize" su "false" verranno preservate le dimensioni originali di queste immagini,
// che occuperà più spazio preservando la qualità dell'immagine.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Guarda anche

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
