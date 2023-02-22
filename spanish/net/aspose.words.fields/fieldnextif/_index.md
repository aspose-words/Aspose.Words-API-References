---
title: Class FieldNextIf
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldNextIf clase. Implementa el campo NEXTIF.
type: docs
weight: 2040
url: /es/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implementa el campo NEXTIF.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Obtiene o establece la parte izquierda de la expresión de comparación. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Obtiene o establece la parte derecha de la expresión de comparación. |
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

Compara los valores designados por las expresiones[`LeftExpression`](./leftexpression/) y[`RightExpression`](./rightexpression/) en comparación usando el operador designado por[`ComparisonOperator`](./comparisonoperator/) . Si la comparación es verdadera, el siguiente registro de datos se fusiona con el documento de fusión actual. (Los campos de combinación que siguen a NEXTIF en el documento main se reemplazan por valores del siguiente registro de datos en lugar del registro de datos actual). Si la comparación es falsa, el siguiente registro de datos se combina en un nuevo documento de combinación.

### Ejemplos

Muestra cómo usar los campos SIGUIENTE/SIGUIENTE para combinar varias filas en una sola página durante una combinación de correspondencia.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea una fuente de datos para nuestra combinación de correspondencia con 3 filas.
    // Una combinación de correspondencia que usa esta tabla normalmente crearía un documento de 3 páginas.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Si tenemos varios campos de combinación con el mismo FieldName,
    // recibirán datos de la misma fila de la fuente de datos y mostrarán el mismo valor después de la combinación.
    // Un campo SIGUIENTE le dice a la combinación de correo instantáneamente que se mueva hacia abajo una fila,
    // lo que significa que cualquier MERGEFIELD que siga al campo NEXT recibirá datos de la siguiente fila.
    // Asegúrese de nunca intentar saltar a la siguiente fila mientras ya está en la última fila.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Después de la fusión, los valores de origen de datos que aceptan estos MERGEFIELD
     // terminará en la misma página que los MERGEFIELD anteriores.
    InsertMergeFields(builder, "Second row: ");

    // Un campo NEXTIF tiene la misma función que un campo NEXT,
    // pero salta a la siguiente fila solo si una declaración construida por las siguientes 3 propiedades es verdadera.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Si la comparación afirmada por el campo anterior es correcta,
    // los siguientes 3 campos de combinación tomarán datos de la tercera fila.
    // De lo contrario, estos campos volverán a tomar datos de la fila 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

      // Nuestra fuente de datos tiene 3 filas y saltamos filas dos veces.
    // Nuestro documento de salida tendrá 1 página con datos de las 3 filas.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");

/// <summary>
/// Utiliza un generador de documentos para insertar MERGEFIELD para una fuente de datos que contiene columnas denominadas "Título de cortesía", "Nombre" y "Apellido".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Utiliza un generador de documentos para insertar un MERRGEFIELD con propiedades específicas.
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


