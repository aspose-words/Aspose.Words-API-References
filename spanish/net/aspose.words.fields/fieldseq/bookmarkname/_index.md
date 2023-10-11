---
title: FieldSeq.BookmarkName
second_title: Referencia de API de Aspose.Words para .NET
description: FieldSeq propiedad. Obtiene o establece un nombre de marcador que hace referencia a un elemento en otra parte del documento en lugar de en la ubicación actual.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Obtiene o establece un nombre de marcador que hace referencia a un elemento en otra parte del documento en lugar de en la ubicación actual.

```csharp
public string BookmarkName { get; set; }
```

### Ejemplos

Muestra cómo combinar tablas de contenido y campos de secuencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC puede crear una entrada en su tabla de contenido para cada campo SEQ que se encuentra en el documento.
// Cada entrada contiene el párrafo que contiene el campo SEQ,
// y el número de la página en la que aparece el campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configure este campo TOC para que tenga una propiedad SequenceIdentifier con un valor de "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configure este campo TOC para seleccionar solo campos SEQ que estén dentro de los límites de un marcador
// llamado "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// Los campos SEQ muestran un recuento que se incrementa en cada campo SEQ.
// Estos campos también mantienen recuentos separados para cada secuencia con nombre única
// identificado por la propiedad "SequenceIdentifier" del campo SEQ.
// Inserta un campo SEQ que tenga un identificador de secuencia que coincida con el TOC
// Propiedad TableOfFiguresLabel. Este campo no creará una entrada en el TOC ya que está fuera
// los límites del marcador designados por "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
// El párrafo que contiene este campo aparecerá en el TOC como una entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La secuencia de este campo SEQ no coincide con la propiedad "TableOfFiguresLabel" del TOC,
// y está dentro de los límites del marcador. Su párrafo no aparecerá en el TOC como entrada.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La secuencia de este campo SEQ coincide con la propiedad "TableOfFiguresLabel" del TOC y está dentro de los límites del marcador.
// Este campo también hace referencia a otro marcador. El contenido de ese marcador aparecerá en la entrada TOC para este campo SEQ.
// El campo SEQ en sí no mostrará el contenido de ese marcador.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Cree un marcador con contenidos que aparecerán en la entrada TOC debido al campo SEQ anterior que hace referencia a él.
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
* espacio de nombres [Aspose.Words.Fields](../../fieldseq/)
* asamblea [Aspose.Words](../../../)


