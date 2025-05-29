---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldAutoNumLgl para una implementación perfecta de campos AUTONUMLGL, mejorando la automatización y el formato de los documentos.
type: docs
weight: 2000
url: /es/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

Implementa el campo AUTONUMLGL.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldAutoNumLgl : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | Obtiene o establece si se debe mostrar el número sin un punto final. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | Obtiene o establece el carácter separador que se utilizará. |
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

Inserta un número automático en formato legal.

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

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
