---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldNextIf implemente de manera eficiente los campos NEXTIF para mejorar la automatización de documentos y optimizar sus flujos de trabajo.
type: docs
weight: 2600
url: /es/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implementa el campo NEXTIF.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldNextIf : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Obtiene o establece el operador de comparación. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Obtiene o establece la parte izquierda de la expresión de comparación. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Obtiene o establece la parte derecha de la expresión de comparación. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
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

Compara los valores designados por las expresiones[`LeftExpression`](./leftexpression/) y[`RightExpression`](./rightexpression/) en comparación utilizando el operador designado por[`ComparisonOperator`](./comparisonoperator/) Si la comparación es verdadera, el siguiente registro de datos se fusiona en el documento de fusión actual. (Los campos de fusión que siguen a NEXTIF en el documento principal se reemplazan con valores del siguiente registro de datos, no del registro actual). Si la comparación es falsa, el siguiente registro de datos se fusiona en un nuevo documento de fusión.

## Ejemplos

Muestra cómo utilizar los campos NEXT/NEXTIF para fusionar varias filas en una página durante una combinación de correspondencia.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Cree una fuente de datos para nuestra combinación de correspondencia con 3 filas.
    // Una combinación de correspondencia que utiliza esta tabla normalmente crearía un documento de 3 páginas.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Si tenemos varios campos de combinación con el mismo FieldName,
    //Recibirán datos de la misma fila de la fuente de datos y mostrarán el mismo valor después de la fusión.
    // Un campo SIGUIENTE le indica al combinador de correspondencia que se mueva instantáneamente hacia abajo una fila,
    // lo que significa que cualquier MERGEFIELD que siga al campo NEXT recibirá datos de la siguiente fila.
    // Asegúrate de nunca intentar saltar a la siguiente fila mientras ya estés en la última fila.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Después de la fusión, los valores de la fuente de datos que estos MERGEFIELDs aceptan
     // terminará en la misma página que los MERGEFIELD anteriores.
    InsertMergeFields(builder, "Second row: ");

    // Un campo NEXTIF tiene la misma función que un campo NEXT,
    // pero salta a la siguiente fila sólo si una declaración construida por las siguientes 3 propiedades es verdadera.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Si la comparación afirmada por el campo anterior es correcta,
    // Los siguientes 3 campos de combinación tomarán datos de la tercera fila.
    // De lo contrario, estos campos tomarán nuevamente datos de la fila 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     //Nuestra fuente de datos tiene 3 filas y omitimos filas dos veces.
    //Nuestro documento de salida tendrá 1 página con datos de las 3 filas.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Utiliza un generador de documentos para insertar MERGEFIELDs para una fuente de datos que contiene columnas denominadas "Título de cortesía", "Nombre" y "Apellido".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Utiliza un generador de documentos para insertar un MERRGEFIELD con propiedades especificadas.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
