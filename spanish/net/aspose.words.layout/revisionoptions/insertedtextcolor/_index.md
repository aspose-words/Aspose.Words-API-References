---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: Aspose.Words para .NET
description: RevisionOptions InsertedTextColor propiedad. Permite especificar el color que se utilizará para el contenido insertado.Insertion . El valor predeterminado esByAuthor  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Permite especificar el color que se utilizará para el contenido insertado.Insertion . El valor predeterminado esByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
```

## Ejemplos

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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
