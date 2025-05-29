---
title: FieldNoteRef.InsertReferenceMark
linktitle: InsertReferenceMark
articleTitle: InsertReferenceMark
second_title: Aspose.Words para .NET
description: Descubra la propiedad InsertReferenceMark de FieldNoteRef para insertar sin problemas marcas de referencia formateadas, mejorando la claridad y el profesionalismo de su documento.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldnoteref/insertreferencemark/
---
## FieldNoteRef.InsertReferenceMark property

Inserta la marca de referencia con el mismo formato de carácter que el estilo Referencia de nota al pie o Referencia de nota final

```csharp
public bool InsertReferenceMark { get; set; }
```

## Ejemplos

Muestra cómo insertar campos NOTEREF y modificar su apariencia.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un marcador con una nota al pie a la que hará referencia el campo NOTEREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Este campo NOTEREF mostrará el número de la nota al pie dentro del marcador referenciado.
    // Establecer la propiedad InsertHyperlink nos permite saltar al marcador presionando Ctrl + clic en el campo en Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Cuando se utiliza el indicador \p, después del número de nota al pie, el campo también muestra la posición del marcador en relación con el campo.
    // Bookmark1 está encima de este campo y contiene la nota al pie número 1, por lo que el resultado será "1 arriba" en la actualización.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 está debajo de este campo y contiene la nota al pie número 2, por lo que el campo mostrará "2 debajo".
    // La bandera \f hace que el número 2 aparezca en el mismo formato que la etiqueta del número de nota al pie en el texto real.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");
}

/// <summary>
/// Utiliza un generador de documentos para insertar un campo NOTEREF con propiedades especificadas.
/// </summary>
private static FieldNoteRef InsertFieldNoteRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, bool insertReferenceMark, string textBefore)
{
    builder.Write(textBefore);

    FieldNoteRef field = (FieldNoteRef)builder.InsertField(FieldType.FieldNoteRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    field.InsertReferenceMark = insertReferenceMark;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utiliza un generador de documentos para insertar un marcador con nombre y una nota al pie al final.
/// </summary>
private static void InsertBookmarkWithFootnote(DocumentBuilder builder, string bookmarkName, string bookmarkText, string footnoteText)
{
    builder.StartBookmark(bookmarkName);
    builder.Write(bookmarkText);
    builder.InsertFootnote(FootnoteType.Footnote, footnoteText);
    builder.EndBookmark(bookmarkName);
    builder.Writeln();
}
```

### Ver también

* class [FieldNoteRef](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
