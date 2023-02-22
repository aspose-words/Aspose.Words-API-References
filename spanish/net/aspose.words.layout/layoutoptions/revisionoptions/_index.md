---
title: LayoutOptions.RevisionOptions
second_title: Referencia de API de Aspose.Words para .NET
description: LayoutOptions propiedad. Obtiene opciones de revisión.
type: docs
weight: 60
url: /es/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Obtiene opciones de revisión.

```csharp
public RevisionOptions RevisionOptions { get; }
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

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../layoutoptions/)
* asamblea [Aspose.Words](../../../)


