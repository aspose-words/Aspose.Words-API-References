---
title: FieldToa.SequenceName
linktitle: SequenceName
articleTitle: SequenceName
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldToa SequenceName para gestionar fácilmente los nombres de secuencia y mejorar la numeración de páginas en sus aplicaciones. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.fields/fieldtoa/sequencename/
---
## FieldToa.SequenceName property

Obtiene o establece el nombre de una secuencia cuyo número está incluido con el número de página.

```csharp
public string SequenceName { get; set; }
```

## Ejemplos

Muestra cómo construir y personalizar una tabla de autoridades utilizando los campos TOA y TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Inserte un campo TOA, que creará una entrada para cada campo TA en el documento,
    // mostrando citas largas y números de página para cada entrada.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Establezca la categoría de entrada para nuestra tabla. Esta TOA ahora solo incluirá campos TA.
    // que tengan un valor coincidente en su propiedad EntryCategory.
    fieldToa.EntryCategory = "1";

    // Además, la categoría de la Tabla de Autoridades en el índice 1 es "Casos",
    // que se mostrará como título de nuestra tabla si establecemos esta variable como verdadera.
    fieldToa.UseHeading = true;

    // Podemos filtrar aún más los campos TA nombrando un marcador que deberá estar dentro de los límites de TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // De manera predeterminada, aparece una pestaña de línea punteada en todo el ancho de la página entre la cita del campo TA
    // y su número de página. Podemos reemplazarlo con cualquier texto que pongamos en esta propiedad.
    // Insertar un carácter de tabulación conservará la tabulación original.
    fieldToa.EntrySeparator = " \t p.";

    // Si tenemos varias entradas de TA que comparten la misma cita larga,
    //Todos sus respectivos números de página se mostrarán en una fila.
    //Podemos usar esta propiedad para especificar una cadena que separará sus números de página.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Podemos establecer esto como verdadero para que nuestra tabla muestre la palabra "passim"
    // si hay cinco o más números de página en una fila.
    fieldToa.UsePassim = true;

    // Un campo TA puede hacer referencia a un rango de páginas.
    // Podemos especificar aquí una cadena para que aparezca entre los números de página inicial y final para dichos rangos.
    fieldToa.PageRangeSeparator = " to ";

    //El formato de los campos TA se trasladará a nuestra tabla.
    //Podemos deshabilitar esto configurando el indicador RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Este campo TA no aparecerá como una entrada en el TOA ya que está fuera
    // los límites del marcador que especifica la propiedad BookmarkName del TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    //Este campo TA está dentro del marcador,
    // pero la categoría de entrada no coincide con la de la tabla, por lo que el campo TA no la incluirá.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    //Esta entrada aparecerá en la tabla.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Una tabla TOA no muestra citas cortas,
    // pero podemos usarlos como una abreviatura para referirnos a nombres de fuentes voluminosos a los que hacen referencia varios campos TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    //Podemos formatear el número de página para ponerlo en negrita/cursiva usando las siguientes propiedades.
    // Aún veremos estos efectos si configuramos nuestra tabla para ignorar el formato.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    //Podemos configurar los campos TA para que sus entradas TOA hagan referencia a un rango de páginas que abarca un marcador.
    // Tenga en cuenta que esta entrada hace referencia a la misma fuente que la anterior para compartir una fila en nuestra tabla.
    // Esta fila tendrá el número de página de la entrada anterior y el rango de páginas de esta entrada,
    // con la lista de páginas de la tabla y los separadores de rango de números de página entre los números de página.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Si hemos habilitado la función "Passim" de nuestra tabla, tener 5 o más entradas TA con la misma fuente la invocará.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Ver también

* class [FieldToa](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
