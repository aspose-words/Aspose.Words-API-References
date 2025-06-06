---
title: FieldTA Class
linktitle: FieldTA
articleTitle: FieldTA
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldTA para una implementación perfecta del campo TA, mejorando sus capacidades de automatización y formato de documentos.
type: docs
weight: 2880
url: /es/net/aspose.words.fields/fieldta/
---
## FieldTA class

Implementa el campo TA.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldTA : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldTA](fieldta/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | Obtiene o establece la categoría de entrada integral, que es un número que corresponde al orden de categorías. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | Obtiene o establece si se debe aplicar formato en negrita al número de página de la entrada. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | Obtiene o establece si se debe aplicar formato en cursiva al número de página de la entrada. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | Obtiene o establece la cita larga para la entrada. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador que marca un rango de páginas que se inserta como número de página de la entrada. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | Obtiene o establece la cita corta de la entrada. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Observaciones

Define el texto y el número de página para una entrada de tabla de autoridades, que se utiliza en un campo TOA.

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

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
