---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words per .NET
description: Scopri il metodo Save di NodeRendererBase. Esegui facilmente il rendering delle forme come immagini e salvale su file per una perfetta integrazione e una maggiore produttività.
type: docs
weight: 90
url: /it/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

Trasforma la forma in un'immagine e la salva in un file.

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file immagine. Se esiste già un file con il nome specificato, il file esistente verrà sovrascritto. |
| saveOptions | ImageSaveOptions | Specifica le opzioni che controllano come la forma viene renderizzata e salvata. Può essere`null`. |

## Esempi

Mostra come eseguire il rendering di un oggetto Office Math in un file immagine nel file system locale.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer del nodo per modificare
// come esegue il rendering del nodo OfficeMath in un'immagine.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Imposta la proprietà "Scala" su 5 per rendere l'oggetto cinque volte più grande della sua dimensione originale.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

Trasforma la forma in un'immagine SVG e la salva in un file.

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome del file immagine. Se esiste già un file con il nome specificato, il file esistente verrà sovrascritto. |
| saveOptions | SvgSaveOptions | Specifica le opzioni che controllano come la forma viene renderizzata e salvata. Può essere`null`. |

## Esempi

Mostra come passare le opzioni di salvataggio durante il rendering di calcoli matematici da ufficio.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Guarda anche

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

Trasforma la forma in un'immagine e la salva in un flusso.

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso in cui salvare l'immagine della forma. |
| saveOptions | ImageSaveOptions | Specifica le opzioni che controllano come la forma viene renderizzata e salvata. Può essere`null` . Se questo è`null`l'immagine verrà salvata nel formato PNG. |

## Esempi

Mostra come utilizzare uno shape renderer per esportare forme in file nel file system locale.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Nel documento sono presenti 7 forme, tra cui una forma di gruppo con 2 forme figlio.
// Renderizzeremo ogni forma in un file immagine nel file system locale
// ignorando le forme del gruppo poiché non hanno alcun aspetto.
// Verranno prodotti 6 file immagine.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

Trasforma la forma in un'immagine SVG e la salva in un flusso.

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso in cui salvare l'immagine SVG della forma. |
| saveOptions | SvgSaveOptions | Specifica le opzioni che controllano come la forma viene renderizzata e salvata. Può essere`null` . Se questo è`null`, l'immagine verrà salvata con le opzioni predefinite. |

## Esempi

Mostra come passare le opzioni di salvataggio durante il rendering di calcoli matematici da ufficio.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### Guarda anche

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
