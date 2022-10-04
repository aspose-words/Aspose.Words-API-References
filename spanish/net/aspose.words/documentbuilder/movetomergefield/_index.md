---
title: MoveToMergeField
second_title: Referencia de API de Aspose.Words para .NET
description: Mueve el cursor a una posición más allá del campo de combinación especificado y elimina el campo de combinación.
type: docs
weight: 530
url: /es/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Mueve el cursor a una posición más allá del campo de combinación especificado y elimina el campo de combinación.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldName | String | El nombre que no distingue entre mayúsculas y minúsculas del campo de combinación de correspondencia. |

### Valor_devuelto

True si se encontró el campo de combinación y se movió el cursor; falso en caso contrario.

### Observaciones

Tenga en cuenta que este método elimina el campo de combinación del documento después de mover el cursor.

### Ejemplos

Muestra cómo llenar MERGEFIELD con datos con un generador de documentos en lugar de una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte algunos MERGEFIELDS, que aceptan datos de columnas del mismo nombre en una fuente de datos durante una combinación de correspondencia,
// y luego llenarlos manualmente.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

Muestra cómo insertar campos de formulario de casilla de verificación en MERGEFIELD como datos de combinación durante la combinación de correspondencia.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Usar MERGEFIELDs con etiquetas "TableStart"/"TableEnd" para definir una región de combinación de correspondencia
    // que pertenece a una fuente de datos denominada "CursoEstudiante" y tiene un MERGEFIELD que acepta datos de una columna denominada "NombreCurso".
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");

/// <summary>
/// Al encontrar un MERGEFIELD con un nombre específico, inserta un campo de formulario de casilla de verificación en lugar de combinar texto de datos.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Llamado cuando una combinación de correo combina datos en un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // En este caso, para cada índice de registro 'n', el valor del campo correspondiente es "Curso n".
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hacer nada.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Crea una fuente de datos de combinación de correspondencia.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Mueve el campo de combinación al campo de combinación especificado.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldName | String | El nombre que no distingue entre mayúsculas y minúsculas del campo de combinación de correspondencia. |
| isAfter | Boolean | Cuando es verdadero, mueve el cursor para que esté después del final del campo. Cuando es falso, mueve el cursor para que esté antes del inicio del campo. |
| isDeleteField | Boolean | Cuando es verdadero, elimina el campo de combinación. |

### Valor_devuelto

True si se encontró el campo de combinación y se movió el cursor; falso en caso contrario.

### Ejemplos

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

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
