---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words per .NET
description: PageSet costruttore. Crea un set di una pagina in base allindice esatto della pagina in C#.
type: docs
weight: 10
url: /it/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Crea un set di una pagina in base all'indice esatto della pagina.

```csharp
public PageSet(int page)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| page | Int32 | Indice in base zero della pagina. |

## Osservazioni

Se viene rilevata una pagina che non è nel documento, verrà generata un'eccezione durante il rendering. MaxValue significa l'ultima pagina del documento.

### Guarda anche

* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Crea un set di pagine in base agli indici di pagina esatti.

```csharp
public PageSet(params int[] pages)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pages | Int32[] | Indici di pagine a base zero. |

## Osservazioni

Se viene rilevata una pagina che non è nel documento, verrà generata un'eccezione durante il rendering. MaxValue significa l'ultima pagina del documento.

## Esempi

Mostra come estrarre le pagine in base agli indici di pagina esatti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge cinque pagine al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Crea un oggetto "XpsSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilizzare la proprietà "PageSet" per selezionare un set di pagine del documento da salvare nell'XPS di output.
// In questo caso sceglieremo, tramite un indice a base zero, solo tre pagine: pagina 1, pagina 2 e pagina 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Guarda anche

* class [PageSet](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Crea un set di pagine in base agli intervalli.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| ranges | PageRange[] | Matrice di intervalli di pagine. |

## Osservazioni

Se viene rilevato un intervallo che inizia dopo l'ultima pagina del documento, verrà generata un'eccezione durante il rendering. Tutti gli intervalli che terminano dopo l'ultima pagina vengono troncati per adattarli al documento.

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
