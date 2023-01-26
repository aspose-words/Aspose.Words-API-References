---
title: InsertField
second_title: Referencia de API de Aspose.Words para .NET
description: Inserta un campo de Word en un documento y opcionalmente actualiza el resultado del campo.
type: docs
weight: 300
url: /es/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

Inserta un campo de Word en un documento y, opcionalmente, actualiza el resultado del campo.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldType | FieldType | El tipo del campo a agregar. |
| updateField | Boolean | Especifica si actualizar el campo inmediatamente. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

### Observaciones

Este método inserta un campo en un documento. Aspose.Words puede actualizar campos de la mayoría de los tipos, pero no todos. Para más detalles ver the `InsertField` sobrecarga.

### Ejemplos

Muestra cómo insertar un campo en un documento usando FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte dos campos mientras pasa una bandera que determina si actualizarlos a medida que el constructor los inserta.
// En algunos casos, la actualización de campos puede ser computacionalmente costosa y puede ser una buena idea posponer la actualización.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Tendremos que actualizar estos campos usando los métodos de actualización manualmente.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

Inserta un campo de Word en un documento y actualiza el resultado del campo.

```csharp
public Field InsertField(string fieldCode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a insertar (sin llaves). |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

### Observaciones

Este método inserta un campo en un documento y actualiza el resultado del campo inmediatamente. Aspose.Words puede actualizar campos de la mayoría de los tipos, pero no todos. Para más detalles ver the `InsertField` sobrecarga.

### Ejemplos

Muestra cómo insertar un campo en un documento utilizando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Muestra cómo insertar campos y mover el cursor del generador de documentos hacia ellos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Mueve el cursor al primer MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Tenga en cuenta que el cursor se coloca inmediatamente después del primer MERGEFIELD y antes del segundo.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Si deseamos editar el código de campo o el contenido del campo usando el constructor,
// su cursor debería estar dentro de un campo.
// Para colocarlo dentro de un campo, necesitaríamos llamar al método MoveTo del generador de documentos
// y pase el nodo de inicio o separador del campo como argumento.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

Inserta un campo de Word en un documento sin actualizar el resultado del campo.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldCode | String | El código de campo a insertar (sin llaves). |
| fieldValue | String | El valor del campo a insertar. Pase nulo para los campos que no tienen un valor. |

### Valor_devuelto

A[`Field`](../../../aspose.words.fields/field/) objeto que representa el campo insertado.

### Observaciones

Los campos en los documentos de Microsoft Word consisten en un código de campo y un resultado de campo. El código de campo es como una fórmula y el resultado de campo es como el valor que produce la fórmula . El código de campo también puede contener switches de campo que son como instrucciones adicionales para realizar una acción específica.

Puede alternar entre mostrar códigos de campo y resultados en su documento en Microsoft Word usando el método abreviado de teclado Alt+F9. Los códigos de campo aparecen entre llaves ( { } ).

Para crear un campo, debe especificar un tipo de campo, un código de campo y un valor de campo de "marcador de posición". Si no está seguro acerca de la sintaxis de un código de campo en particular, cree el campo en Microsoft Word primero y cambie para ver su código de campo .

Aspose.Words puede calcular los resultados de los campos para la mayoría de los tipos de campos, pero este method no actualiza el resultado del campo automáticamente. Debido a que el resultado del campo no se calcula automáticamente, se espera que pase algún valor de cadena (o incluso una cadena vacía) que se insertará en el resultado del campo. Este valor permanecerá en el resultado del campo como un marcador de posición hasta que el campo sea actualizado. Para actualizar el resultado del campo puede llamar[`Update`](../../../aspose.words.fields/field/update/)en el objeto de campo devuelto a usted o[`UpdateFields`](../../document/updatefields/) para actualizar campos en todo el documento.

### Ejemplos

Muestra cómo configurar la numeración de páginas en una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Mover el generador de documentos al encabezado principal de la primera sección,
// que se mostrará en todas las páginas de esa sección.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Inserta un campo de PÁGINA, que mostrará el número de la página actual.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Configure la sección para que el recuento de páginas que muestran los campos de PÁGINA comience desde 5.
// Además, configure todos los campos de PÁGINA para mostrar sus números de página usando números romanos en mayúsculas.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Cree otro encabezado principal para la segunda sección, con otro campo de PÁGINA.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Configure la sección para que el recuento de páginas que muestran los campos de PÁGINA comience desde 10.
// Además, configure todos los campos de PÁGINA para mostrar sus números de página usando números arábigos.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Ver también

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
