---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words per .NET
description: Crea senza sforzo un set di pagine personalizzate con il costruttore PageSet, progettato per un'indicizzazione precisa delle pagine e un'esperienza utente fluida.
type: docs
weight: 10
url: /it/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Crea un set di una pagina basato sull'indice di pagina esatto.

```csharp
public PageSet(int page)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| page | Int32 | Indice della pagina basato su zero. |

## Osservazioni

Se viene rilevata una pagina non presente nel documento, verrà generata un'eccezione durante il rendering. MaxValue indica l'ultima pagina del documento.

## Esempi

Mostra come convertire una pagina di un documento in un'immagine JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Creiamo un oggetto "ImageSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo trasforma il documento in un'immagine.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Imposta "PageSet" su "1" per selezionare la seconda pagina tramite
// l'indice a partire da zero da cui iniziare il rendering del documento.
options.PageSet = new PageSet(1);

// Quando salviamo il documento nel formato JPEG, Aspose.Words esegue il rendering di una sola pagina.
// Questa immagine conterrà una pagina a partire da pagina due,
// che sarà semplicemente la seconda pagina del documento originale.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Guarda anche

* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Crea un set di pagine basato sugli indici di pagina esatti.

```csharp
public PageSet(params int[] pages)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pages | Int32[] | Indici di pagina basati su zero. |

## Osservazioni

Se viene rilevata una pagina non presente nel documento, verrà generata un'eccezione durante il rendering. MaxValue indica l'ultima pagina del documento.

## Esempi

Mostra come estrarre le pagine in base agli indici di pagina esatti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungere cinque pagine al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Creiamo un oggetto "XpsSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilizzare la proprietà "PageSet" per selezionare un set di pagine del documento da salvare in output XPS.
// In questo caso, sceglieremo, tramite un indice a partire da zero, solo tre pagine: pagina 1, pagina 2 e pagina 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Guarda anche

* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Crea un set di pagine basato su intervalli.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| ranges | PageRange[] | Serie di intervalli di pagine. |

## Osservazioni

Se viene rilevato un intervallo che inizia dopo l'ultima pagina del documento, verrà generata un'eccezione durante il rendering. Tutti gli intervalli che terminano dopo l'ultima pagina vengono troncati per adattarsi al documento.

## Esempi

Mostra come estrarre le pagine in base a intervalli di pagine esatti.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Guarda anche

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
