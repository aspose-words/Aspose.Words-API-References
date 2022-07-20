---
title: FieldMergeField
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo MERGEFIELD.
type: docs
weight: 2000
url: /es/net/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class

Implementa el campo MERGEFIELD.

```csharp
public class FieldMergeField : Field
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtiene el nodo que representa el final del campo. |
| [FieldName](../../aspose.words.fields/fieldmergefield/fieldname) { get; set; } | Obtiene o establece el nombre de un campo de datos. |
| [FieldNameNoPrefix](../../aspose.words.fields/fieldmergefield/fieldnamenoprefix) { get; } | Devuelve solo el nombre del campo de datos. Cualquier prefijo se elimina a la propiedad de prefijo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtiene un[`FieldFormat`](../fieldformat) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [IsMapped](../../aspose.words.fields/fieldmergefield/ismapped) { get; set; } | Obtiene o establece si este campo es un campo asignado. |
| [IsVerticalFormatting](../../aspose.words.fields/fieldmergefield/isverticalformatting) { get; set; } | Obtiene o establece si habilitar la conversión de caracteres para formato vertical. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TextAfter](../../aspose.words.fields/fieldmergefield/textafter) { get; set; } | Obtiene o establece el texto que se insertará después del campo si el campo no está en blanco. |
| [TextBefore](../../aspose.words.fields/fieldmergefield/textbefore) { get; set; } | Obtiene o establece el texto que se insertará antes del campo si el campo no está en blanco. |
| override [Type](../../aspose.words.fields/fieldmergefield/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Recupera el nombre de un campo de datos dentro de los caracteres de combinación en un documento principal de combinación de correspondencia. Cuando el documento principal se combina con la fuente de datos seleccionada, la información del campo de datos especificado se inserta en lugar del campo de combinación.

### Ejemplos

Muestra cómo utilizar los campos MERGEFIELD para realizar una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Cree una tabla de datos para usarla como fuente de datos de combinación de correspondencia.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Inserte un MERGEFIELD con una propiedad FieldName establecida en el nombre de una columna en la fuente de datos.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// Podemos aplicar texto antes y después del valor que acepta este campo cuando se produce la fusión.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// Inserte otro MERGEFIELD para una columna diferente en la fuente de datos.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### Ver también

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
