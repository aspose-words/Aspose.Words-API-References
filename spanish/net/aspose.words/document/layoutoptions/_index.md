---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words para .NET
description: Document LayoutOptions propiedad. Obtiene unLayoutOptions objeto que representa opciones para controlar el proceso de diseño de este documento en C#.
type: docs
weight: 250
url: /es/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Obtiene un[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) objeto que representa opciones para controlar el proceso de diseño de este documento.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Ejemplos

Muestra cómo ocultar texto en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Inserta texto oculto, luego especifica si deseamos omitirlo en un documento renderizado.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

Muestra cómo mostrar marcas de párrafo en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Agrega algunos párrafos, luego habilita las marcas de párrafo para mostrar los finales de los párrafos
// con un símbolo pilcrow (¶) cuando renderizamos el documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

Muestra cómo alterar la apariencia de las revisiones en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una revisión, luego cambia el color de todas las revisiones a verde.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Elimina la barra que aparece a la izquierda de cada línea revisada.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ver también

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
