---
title: ImageSaveOptions.PageSet
second_title: Aspose.Words per .NET API Reference
description: ImageSaveOptions proprietà. Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento.
type: docs
weight: 90
url: /it/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento.

```csharp
public PageSet PageSet { get; set; }
```

### Osservazioni

Questa proprietà ha effetto solo durante il rendering delle pagine del documento. Questa proprietà viene ignorata durante il rendering di forme in immagini.

### Esempi

Mostra come estrarre le pagine in base a intervalli di pagine esatti.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

Mostra come eseguire il rendering di ogni pagina di un documento in un'immagine TIFF separata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // Imposta la proprietà "PageSet" sul numero della prima pagina da
    // da cui iniziare il rendering del documento.
    options.PageSet = new PageSet(i);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

Mostra come specificare la pagina di un documento di cui eseguire il rendering come immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// Quando salviamo il documento come immagine, Aspose.Words esegue il rendering solo della prima pagina per impostazione predefinita.
// Possiamo passare un oggetto SaveOptions per specificare una pagina diversa da visualizzare.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);

// Rendering di ogni pagina del documento in un file immagine separato.
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

Mostra come eseguire il rendering di una pagina da un documento a un'immagine JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un oggetto "ImageSaveOptions" che possiamo passare al metodo "Salva" del documento
// per modificare il modo in cui quel metodo esegue il rendering del documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// Imposta "PageSet" su "1" per selezionare la seconda pagina tramite
// l'indice in base zero da cui iniziare il rendering del documento.
options.PageSet = new PageSet(1);

// Quando salviamo il documento nel formato JPEG, Aspose.Words esegue il rendering di una sola pagina.
// Questa immagine conterrà una pagina a partire dalla seconda pagina,
// che sarà solo la seconda pagina del documento originale.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Guarda anche

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../imagesaveoptions/)
* assemblea [Aspose.Words](../../../)


