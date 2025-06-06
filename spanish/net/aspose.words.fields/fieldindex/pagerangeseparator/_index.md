---
title: FieldIndex.PageRangeSeparator
linktitle: PageRangeSeparator
articleTitle: PageRangeSeparator
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageRangeSeparator en FieldIndex. Personalice fácilmente la secuencia de caracteres para un formato uniforme del rango de páginas y mejore la claridad de su documento.
type: docs
weight: 130
url: /es/net/aspose.words.fields/fieldindex/pagerangeseparator/
---
## FieldIndex.PageRangeSeparator property

Obtiene o establece la secuencia de caracteres que se utiliza para separar el inicio y el final de un rango de páginas.

```csharp
public string PageRangeSeparator { get; set; }
```

## Ejemplos

Muestra cómo especificar las páginas abarcadas por un marcador como un rango de páginas para una entrada del campo ÍNDICE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree un campo INDEX que mostrará una entrada para cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad de Texto del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Texto"
// en una sola entrada en lugar de hacer una entrada para cada campo XE.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Para las entradas INDEX que muestran rangos de páginas, podemos especificar una cadena separadora
// que aparecerá entre el número de la primera página y el número de la última.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Si un campo XE nombra un marcador utilizando la propiedad PageRangeBookmarkName,
// su entrada INDEX mostrará el rango de páginas que abarca el marcador
// en lugar del número de la página que contiene el campo XE.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Inserta un marcador que comienza en la página 3 y termina en la página 5.
// La entrada INDEX del campo XE que hace referencia a este marcador mostrará este rango de páginas.
// En nuestra tabla, la entrada INDEX mostrará "Mi entrada, en las páginas 3 a 5".
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Ver también

* class [FieldIndex](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
