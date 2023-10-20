---
title: FieldNextIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words para .NET
description: FieldNextIf RightExpression propiedad. Obtiene o establece la parte derecha de la expresión de comparación en C#.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

Obtiene o establece la parte derecha de la expresión de comparación.

```csharp
public string RightExpression { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos SIGUIENTE/SIGUIENTEIF para combinar varias filas en una página durante una combinación de correspondencia.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea una fuente de datos para nuestra combinación de correspondencia con 3 filas.
    // Una combinación de correspondencia que utilice esta tabla normalmente crearía un documento de 3 páginas.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Si tenemos varios campos combinados con el mismo nombre de campo,
    // recibirán datos de la misma fila de la fuente de datos y mostrarán el mismo valor después de la combinación.
    // Un campo SIGUIENTE le indica a la combinación de correspondencia que baje instantáneamente una fila,
    // lo que significa que cualquier MERGEFIELD que siga al campo SIGUIENTE recibirá datos de la siguiente fila.
    // Asegúrate de nunca intentar saltar a la siguiente fila mientras ya estás en la última fila.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Después de la fusión, los valores de la fuente de datos que aceptan estos MERGEFIELD
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
    // los siguientes 3 campos de combinación tomarán datos de la tercera fila.
    // De lo contrario, estos campos volverán a tomar datos de la fila 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Nuestra fuente de datos tiene 3 filas y nos saltamos filas dos veces.
    // Nuestro documento de salida tendrá 1 página con datos de las 3 filas.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

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

* class [FieldNextIf](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
