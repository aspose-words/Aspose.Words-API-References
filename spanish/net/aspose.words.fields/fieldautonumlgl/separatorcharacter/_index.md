---
title: FieldAutoNumLgl.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar la propiedad FieldAutoNumLgl SeparatorCharacter para mejorar el formato de sus datos con un carácter separador flexible.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Obtiene o establece el carácter separador que se utilizará.

```csharp
public string SeparatorCharacter { get; set; }
```

## Ejemplos

Muestra cómo organizar un documento utilizando campos AUTONUMLGL.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // Los campos AUTONUMLGL muestran un número que se incrementa en cada campo AUTONUMLGL dentro de su nivel de encabezado actual.
    // Estos campos mantienen un recuento separado para cada nivel de encabezado,
     // y cada campo también muestra los recuentos de campos AUTONUMLGL para todos los niveles de encabezado debajo del suyo.
    // Cambiar el recuento de cualquier nivel de encabezado restablece los recuentos de todos los niveles por encima de ese nivel a 1.
    // Esto nos permite organizar nuestro documento en forma de lista de esquema.
    // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 1, que muestra "1." en el documento.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Este es el segundo campo AUTONUMLGL en un nivel de encabezado de 1, por lo que mostrará "2".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 2,
    // y el recuento AUTONUMLGL para el nivel de encabezado debajo es "2", por lo que mostrará "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Este es el primer campo AUTONUMLGL en un nivel de encabezado de 3.
    // Trabajando de la misma manera que el campo anterior, mostrará "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Este campo está en un nivel de encabezado de 2, y su respectivo recuento AUTONUMLGL está en 2, por lo que el campo mostrará "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incrementar el recuento de AUTONUMLGL para un nivel de encabezado por debajo de este
    // ha restablecido el recuento para este nivel para que este campo muestre "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // El carácter separador, que aparece en el campo resultado inmediatamente después del número,
        // es un punto por defecto. Si dejamos esta propiedad nula,
        //Nuestro último campo AUTONUMLGL mostrará "2.2.1." en el documento.
        Assert.IsNull(field.SeparatorCharacter);

        // Establecer un carácter separador personalizado y eliminar el punto final
        // cambiará la apariencia de ese campo de "2.2.1." a "2:2:1".
        // Aplicaremos esto a todos los campos que hemos creado.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Utiliza un generador de documentos para insertar una cláusula numerada por un campo AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    //Este texto pertenecerá al campo legal de numeración automática que se encuentra encima de él.
    //Se colapsará cuando hagamos clic en la flecha junto al campo AUTONUMLGL correspondiente en Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Ver también

* class [FieldAutoNumLgl](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
