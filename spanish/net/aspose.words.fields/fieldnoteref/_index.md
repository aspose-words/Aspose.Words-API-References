---
title: Class FieldNoteRef
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldNoteRef clase. Implementa el campo NOTEREF.
type: docs
weight: 2050
url: /es/net/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class

Implementa el campo NOTEREF.

```csharp
public class FieldNoteRef : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldNoteRef](fieldnoteref/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldnoteref/bookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [InsertHyperlink](../../aspose.words.fields/fieldnoteref/inserthyperlink/) { get; set; } | Obtiene o establece si se inserta un hipervínculo al párrafo marcado. |
| [InsertReferenceMark](../../aspose.words.fields/fieldnoteref/insertreferencemark/) { get; set; } | Inserta la marca de referencia con el mismo formato de carácter que el estilo Referencia de nota al pie o Referencia de nota al final. |
| [InsertRelativePosition](../../aspose.words.fields/fieldnoteref/insertrelativeposition/) { get; set; } | Obtiene o establece si se inserta una posición relativa del párrafo marcado. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Inserta la marca de la nota al pie o al final marcada por el marcador especificado.

### Ejemplos

Muestra para insertar campos NOTEREF y modificar su apariencia.

```csharp
public void FieldNoteRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Cree un marcador con una nota al pie de página a la que hará referencia el campo NOTEREF.
    InsertBookmarkWithFootnote(builder, "MyBookmark1", "Contents of MyBookmark1", "Footnote from MyBookmark1");

    // Este campo NOTEREF mostrará el número de la nota al pie dentro del marcador al que se hace referencia.
    // Establecer la propiedad InsertHyperlink nos permite saltar al marcador presionando Ctrl + haciendo clic en el campo en Microsoft Word.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h",
        InsertFieldNoteRef(builder, "MyBookmark2", true, false, false, "Hyperlink to Bookmark2, with footnote number ").GetFieldCode());

    // Al usar el indicador \p, después del número de nota al pie, el campo también muestra la posición del marcador en relación con el campo.
    // Bookmark1 está encima de este campo y contiene la nota al pie número 1, por lo que el resultado será "1 arriba" en la actualización.
    Assert.AreEqual(" NOTEREF  MyBookmark1 \\h \\p",
        InsertFieldNoteRef(builder, "MyBookmark1", true, true, false, "Bookmark1, with footnote number ").GetFieldCode());

    // Bookmark2 está debajo de este campo y contiene la nota al pie número 2, por lo que el campo mostrará "2 debajo".
    // La bandera \f hace que el número 2 aparezca en el mismo formato que la etiqueta del número de la nota al pie en el texto real.
    Assert.AreEqual(" NOTEREF  MyBookmark2 \\h \\p \\f",
        InsertFieldNoteRef(builder, "MyBookmark2", true, true, true, "Bookmark2, with footnote number ").GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);
    InsertBookmarkWithFootnote(builder, "MyBookmark2", "Contents of MyBookmark2", "Footnote from MyBookmark2");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.NOTEREF.docx");

/// <summary>
/// Utiliza un generador de documentos para insertar un campo NOTEREF con propiedades específicas.
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
/// Utiliza un generador de documentos para insertar un marcador con nombre con una nota al pie al final.
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

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


