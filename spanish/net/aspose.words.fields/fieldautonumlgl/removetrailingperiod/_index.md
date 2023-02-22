---
title: FieldAutoNumLgl.RemoveTrailingPeriod
second_title: Referencia de API de Aspose.Words para .NET
description: FieldAutoNumLgl propiedad. Obtiene o establece si mostrar el número sin un punto final.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

Obtiene o establece si mostrar el número sin un punto final.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

### Ejemplos

Muestra cómo organizar un documento usando campos AUTONUMLGL.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // Los campos AUTONUMLGL muestran un número que se incrementa en cada campo AUTONUMLGL dentro de su nivel de encabezado actual.
    // Estos campos mantienen un conteo separado para cada nivel de encabezado,
      // y cada campo también muestra el recuento de campos AUTONUMLGL para todos los niveles de encabezado por debajo del suyo.
    // Al cambiar el recuento de cualquier nivel de encabezado, se restablecen los recuentos de todos los niveles por encima de ese nivel a 1.
    // Esto nos permite organizar nuestro documento en forma de una lista de esquemas.
    // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 1, que muestra "1". en el documento
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Este es el segundo campo AUTONUMLGL con un nivel de encabezado de 1, por lo que mostrará "2".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 2,
    // y el recuento de AUTONUMLGL para el nivel de título inferior es "2", por lo que mostrará "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

      // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 3.
    // Trabajando de la misma manera que el campo anterior, mostrará "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Este campo tiene un nivel de encabezado de 2 y su cuenta AUTONUMLGL respectiva es de 2, por lo que el campo mostrará "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incrementando el conteo AUTONUMLGL para un nivel de encabezado por debajo de este
    // ha restablecido el recuento de este nivel para que este campo muestre "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // El carácter separador, que aparece en el resultado del campo inmediatamente después del número,
        // es un punto por defecto. Si dejamos esta propiedad nula,
        // nuestro último campo AUTONUMLGL mostrará "2.2.1". en el documento
        Assert.IsNull(field.SeparatorCharacter);

        // Establecer un carácter separador personalizado y eliminar el punto final
        // cambiará la apariencia de ese campo de "2.2.1". a "2:2:1".
        // Aplicaremos esto a todos los campos que hayamos creado.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// Utiliza un generador de documentos para insertar una cláusula numerada por un campo AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Este texto pertenecerá al campo legal de numeración automática que se encuentra arriba.
    // Se colapsará cuando hagamos clic en la flecha al lado del campo AUTONUMLGL correspondiente en Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Ver también

* class [FieldAutoNumLgl](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldautonumlgl/)
* asamblea [Aspose.Words](../../../)


