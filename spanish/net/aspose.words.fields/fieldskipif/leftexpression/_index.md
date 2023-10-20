---
title: FieldSkipIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words para .NET
description: FieldSkipIf LeftExpression propiedad. Obtiene o establece la parte izquierda de la expresión de comparación en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldskipif/leftexpression/
---
## FieldSkipIf.LeftExpression property

Obtiene o establece la parte izquierda de la expresión de comparación.

```csharp
public string LeftExpression { get; set; }
```

## Ejemplos

Muestra cómo omitir páginas en una combinación de correspondencia usando el campo SKIPIF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un campo SKIPIF. Si la fila actual de una operación de combinación de correspondencia cumple la condición
// que indican las expresiones de este campo, entonces la operación de combinación de correspondencia aborta la fila actual,
// descarta el documento de combinación actual y luego pasa inmediatamente a la siguiente fila para comenzar el siguiente documento de combinación.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Mueve el constructor al separador del campo SKIPIF para que podamos colocar un MERGEFIELD dentro del campo SKIPIF.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD se refiere a la columna "Departamento" en nuestra tabla de datos. Si una fila de esa tabla
// tiene un valor de "HR" en su columna "Departamento", entonces esta fila cumplirá la condición.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Agrega contenido a nuestro documento, crea la fuente de datos y ejecuta la combinación de correspondencia.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Esta tabla tiene tres filas y una de ellas cumple la condición de nuestro campo SKIPIF.
// La combinación de correspondencia producirá dos páginas.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Muestra cómo utilizar los campos MERGEREC y MERGESEQ para numerar y contar registros de combinación de correspondencia en los documentos de salida de una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Un campo MERGEREC imprimirá el número de fila de los datos que se fusionan en cada documento de salida de la combinación.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Un campo MERGESEQ contará el número de fusiones exitosas e imprimirá el valor actual en cada página respectiva.
// Si una combinación de correspondencia no omite ninguna fila y no invoca ningún campo SKIP/SKIPIF/NEXT/NEXTIF, todas las combinaciones se realizan correctamente.
// Los campos MERGESEQ y MERGEREC mostrarán los mismos resultados si la combinación de correspondencia fue exitosa.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Inserta un campo SKIPIF, que omitirá una combinación si el nombre es "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Crea una fuente de datos con 3 filas, una de ellas con "John Doe" como valor para la columna "Nombre".
// Dado que un campo SKIPIF se activará una vez con ese valor, el resultado de nuestra combinación de correspondencia tendrá 2 páginas en lugar de 3.
// En la página 1, los campos MERGESEQ y MERGEREC mostrarán "1".
// En la página 2, el campo MERGEREC mostrará "3" y el campo MERGESEQ mostrará "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Ver también

* class [FieldSkipIf](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
