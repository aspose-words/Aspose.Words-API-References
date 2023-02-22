---
title: RevisionOptions.InsertedTextColor
second_title: Referencia de API de Aspose.Words para .NET
description: RevisionOptions propiedad. Permite especificar el color que se utilizará para el contenido insertadoInsertion . El valor predeterminado esByAuthor .
type: docs
weight: 40
url: /es/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Permite especificar el color que se utilizará para el contenido insertadoInsertion . El valor predeterminado esByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
```

### Ejemplos

Muestra cómo modificar la apariencia de las revisiones en un documento de salida renderizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte una revisión, luego cambie el color de todas las revisiones a verde.
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
* espacio de nombres [Aspose.Words.Layout](../../revisionoptions/)
* asamblea [Aspose.Words](../../../)


