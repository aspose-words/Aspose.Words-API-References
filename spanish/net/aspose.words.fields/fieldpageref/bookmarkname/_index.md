---
title: FieldPageRef.BookmarkName
second_title: Referencia de API de Aspose.Words para .NET
description: FieldPageRef propiedad. Obtiene o establece el nombre del marcador.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldpageref/bookmarkname/
---
## FieldPageRef.BookmarkName property

Obtiene o establece el nombre del marcador.

```csharp
public string BookmarkName { get; set; }
```

### Ejemplos

Muestra para insertar campos PAGEREF para mostrar la ubicación relativa de los marcadores.

```csharp
public void FieldPageRef()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);            

    InsertAndNameBookmark(builder, "MyBookmark1");

    // Inserta un campo PAGEREF que muestra en qué página se encuentra un marcador.
    // Establece el indicador InsertHyperlink para que el campo también funcione como un enlace al marcador en el que se puede hacer clic.
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h", 
        InsertFieldPageRef(builder, "MyBookmark3", true, false, "Hyperlink to Bookmark3, on page: ").GetFieldCode());

    // Podemos usar el indicador \p para mostrar el campo PAGEREF
    // la posición del marcador en relación con la posición del campo.
    // Bookmark1 está en la misma página y encima de este campo, por lo que el resultado mostrado de este campo estará "arriba".
    Assert.AreEqual(" PAGEREF  MyBookmark1 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark1", true, true, "Bookmark1 is ").GetFieldCode());

    // Bookmark2 estará en la misma página y debajo de este campo, por lo que el resultado mostrado de este campo estará "abajo".
    Assert.AreEqual(" PAGEREF  MyBookmark2 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark2", true, true, "Bookmark2 is ").GetFieldCode());

    // Bookmark3 estará en una página diferente, por lo que el campo se mostrará "en la página 2".
    Assert.AreEqual(" PAGEREF  MyBookmark3 \\h \\p", 
        InsertFieldPageRef(builder, "MyBookmark3", true, true, "Bookmark3 is ").GetFieldCode());

    InsertAndNameBookmark(builder, "MyBookmark2");
    builder.InsertBreak(BreakType.PageBreak);
    InsertAndNameBookmark(builder, "MyBookmark3");

    doc.UpdatePageLayout();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.PAGEREF.docx");
}

/// <summary>
/// Utiliza un generador de documentos para insertar un campo PAGEREF y establece sus propiedades.
/// </summary>
private static FieldPageRef InsertFieldPageRef(DocumentBuilder builder, string bookmarkName, bool insertHyperlink, bool insertRelativePosition, string textBefore)
{
    builder.Write(textBefore);

    FieldPageRef field = (FieldPageRef)builder.InsertField(FieldType.FieldPageRef, true);
    field.BookmarkName = bookmarkName;
    field.InsertHyperlink = insertHyperlink;
    field.InsertRelativePosition = insertRelativePosition;
    builder.Writeln();

    return field;
}

/// <summary>
/// Utiliza un generador de documentos para insertar un marcador con nombre.
/// </summary>
private static void InsertAndNameBookmark(DocumentBuilder builder, string bookmarkName)
{
    builder.StartBookmark(bookmarkName);
    builder.Writeln($"Contents of bookmark \"{bookmarkName}\".");
    builder.EndBookmark(bookmarkName);
}
```

### Ver también

* class [FieldPageRef](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldpageref/)
* asamblea [Aspose.Words](../../../)


