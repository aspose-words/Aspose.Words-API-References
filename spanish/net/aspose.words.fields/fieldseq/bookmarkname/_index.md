---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldSeq BookmarkName para gestionar fácilmente la navegación por documentos. Establezca o recupere nombres de marcadores para una referencia fluida de elementos.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Obtiene o establece un nombre de marcador que hace referencia a un elemento en otra parte del documento en lugar de en la ubicación actual.

```csharp
public string BookmarkName { get; set; }
```

## Ejemplos

Muestra cómo combinar campos de tabla de contenido y de secuencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ encontrado en el documento.
// Cada entrada contiene el párrafo que contiene el campo SEQ,
// y el número de la página en la que aparece el campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configure este campo TOC para tener una propiedad SequenceIdentifier con un valor de "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configure este campo TOC para seleccionar únicamente los campos SEQ que estén dentro de los límites de un marcador
// llamado "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre único
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserte un campo SEQ que tenga un identificador de secuencia que coincida con la tabla de contenidos
// Propiedad TableOfFiguresLabel. Este campo no creará una entrada en la tabla de contenidos, ya que está fuera de ella.
// los límites del marcador designados por "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos y está dentro de los límites del marcador.
// El párrafo que contiene este campo aparecerá en la tabla de contenidos como una entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La secuencia de este campo SEQ no coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos.
// y está dentro de los límites del marcador. Su párrafo no aparecerá en la tabla de contenidos como entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" de la tabla de contenidos y está dentro de los límites del marcador.
Este campo también hace referencia a otro marcador. El contenido de ese marcador aparecerá en la entrada de la tabla de contenidos de este campo de secuencia.
//El campo SEQ en sí no mostrará el contenido de ese marcador.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Cree un marcador con contenidos que se mostrarán en la entrada TOC debido a que el campo SEQ anterior hace referencia a él.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Ver también

* class [FieldSeq](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
