---
title: FieldMergingArgsBase.TableName
linktitle: TableName
articleTitle: TableName
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldMergingArgsBase TableName, acceda fácilmente al nombre de la tabla de datos para sus operaciones de combinación o sepa cuándo no está disponible.
type: docs
weight: 70
url: /es/net/aspose.words.mailmerging/fieldmergingargsbase/tablename/
---
## FieldMergingArgsBase.TableName property

Obtiene el nombre de la tabla de datos para la operación de combinación actual o una cadena vacía si el nombre no está disponible.

```csharp
public string TableName { get; }
```

## Ejemplos

Muestra cómo insertar campos de formulario de casilla de verificación en MERGEFIELDs como datos de combinación durante la combinación de correspondencia.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Utilice MERGEFIELDs con etiquetas "TableStart"/"TableEnd" para definir una región de combinación de correspondencia
    // que pertenece a una fuente de datos denominada "StudentCourse" y tiene un MERGEFIELD que acepta datos de una columna denominada "CourseName".
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
}

/// <summary>
/// Al encontrar un MERGEFIELD con un nombre específico, inserta un campo de formulario de casilla de verificación en lugar de texto de datos combinados.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Se llama cuando una combinación de correspondencia fusiona datos en un MERGEFIELD.
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
        //No hacer nada.
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

* class [FieldMergingArgsBase](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
