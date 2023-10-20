---
title: ImageSaveOptions.Scale
linktitle: Scale
articleTitle: Scale
second_title: Aspose.Words per .NET
description: ImageSaveOptions Scale proprietà. Ottiene o imposta il fattore di zoom per le immagini generate in C#.
type: docs
weight: 150
url: /it/net/aspose.words.saving/imagesaveoptions/scale/
---
## ImageSaveOptions.Scale property

Ottiene o imposta il fattore di zoom per le immagini generate.

```csharp
public float Scale { get; set; }
```

## Osservazioni

Il valore predefinito è 1.0. Il valore deve essere maggiore di 0.

## Esempi

Mostra come eseguire il rendering di un oggetto Office Math in un file di immagine nel file system locale.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer del nodo per modificare
// come esegue il rendering del nodo OfficeMath in un'immagine.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Imposta la proprietà "Scala" su 5 per rendere l'oggetto cinque volte la sua dimensione originale.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

Mostra come modificare l'immagine mentre Aspose.Words converte un documento in uno.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio ne esegue il rendering.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png)
{
    // Possiamo regolare queste proprietà per modificare la luminosità e il contrasto dell'immagine.
    // Entrambi sono su una scala 0-1 e sono a 0,5 per impostazione predefinita.
    ImageBrightness = 0.3f,
    ImageContrast = 0.7f,

    // Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
    // Ciò influenzerà le dimensioni dell'immagine.
    // Il valore predefinito per queste proprietà è 96.0, per una risoluzione di 96 dpi.
    HorizontalResolution = 72f,
    VerticalResolution = 72f,

    // Possiamo ridimensionare l'immagine utilizzando questa proprietà. Il valore predefinito è 1,0, per un ridimensionamento del 100%.
    // Possiamo utilizzare questa proprietà per annullare eventuali modifiche nelle dimensioni dell'immagine che la modifica della risoluzione causerebbe.
    Scale = 96f / 72f
};

doc.Save(ArtifactsDir + "ImageSaveOptions.EditImage.png", options);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
