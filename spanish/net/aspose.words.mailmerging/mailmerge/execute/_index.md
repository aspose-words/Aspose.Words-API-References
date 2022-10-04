---
title: Execute
second_title: Referencia de API de Aspose.Words para .NET
description: Realiza una combinación de correspondencia desde una fuente de datos personalizada.
type: docs
weight: 180
url: /es/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(IMailMergeDataSource) {#execute}

Realiza una combinación de correspondencia desde una fuente de datos personalizada.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un objeto que implementa la interfaz de fuente de datos de combinación de correspondencia personalizada. |

### Observaciones

Utilice este método para completar los campos de combinación de correspondencia en el documento con valores de cualquier fuente de datos, como una lista, una tabla hash u objetos. Necesitas escribir tu propia clase que implementa el[`IMailMergeDataSource`](../../imailmergedatasource/) interfaz.

Puede utilizar este método sólo cuando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)es falso, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

Este método ignora laRemoveUnusedRegions opción.

### Ver también

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## Execute(string[], object[]) {#execute_5}

Realiza una operación de combinación de correspondencia para un solo registro.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldNames | String[] | Matriz de nombres de campos de combinación. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| values | Object[] | Matriz de valores que se insertará en los campos de combinación. El número de elementos en esta matriz debe ser el mismo que el número de elementos en fieldNames. |

### Observaciones

Utilice este método para completar los campos de combinación de correspondencia en el documento con valores de una matriz de objetos.

Este método fusiona datos para un solo registro. La matriz de nombres de campo y la matriz de valores representan los datos de un solo registro.

Este método no utiliza regiones de combinación de correspondencia.

Este método ignora laRemoveUnusedRegions opción.

### Ejemplos

Muestra cómo combinar una imagen de un URI como datos de combinación de correspondencia en un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// MERGEFIELDs con etiquetas "Imagen:" recibirán una imagen durante una combinación de correspondencia.
// La cadena después de los dos puntos en la etiqueta "Imagen:" corresponde a un nombre de columna
// en la fuente de datos cuyas celdas contienen URI de archivos de imagen.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

  // Cree una fuente de datos que contenga URI de imágenes que fusionaremos.
// Un URI puede ser una URL web que apunte a una imagen o un nombre de archivo del sistema de archivos local de un archivo de imagen.
string[] columns = { "logo_FromWeb", "logo_FromFileSystem" };
object[] URIs = { ImageUrl, ImageDir + "Logo.jpg" };

// Ejecutar una combinación de correspondencia en una fuente de datos con una fila.
doc.MailMerge.Execute(columns, URIs);

doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromUrl.docx");
```

Muestra cómo realizar una combinación de correspondencia y luego guardar el documento en el navegador del cliente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Envía el documento al navegador del cliente.
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Lanzado porque HttpResponse es nulo en la prueba.

// Tendremos que cerrar esta respuesta manualmente para asegurarnos de no agregar ningún contenido superfluo al documento después de guardarlo.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## Execute(DataTable) {#execute_2}

Realiza la combinación de correspondencia de un DataTable en el documento.

```csharp
public void Execute(DataTable table)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| table | DataTable | Tabla que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de los campos no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |

### Observaciones

Use este método para completar los campos de combinación de correspondencia en el documento con valores de a  **Tabla de datos**.

Todos los registros de la tabla se combinan en el documento.

Puede usar el campo SIGUIENTE en el documento de Word para causar **Unificación de correo** objeto para seleccionar siguiente registro del **Tabla de datos** y continuar fusionando. Esto se puede usar al crear documentos como etiquetas postales.

Cuando **Unificación de correo**el objeto llega al final del documento principal y todavía hay más filas en el **Tabla de datos**, copia todo el contenido de el documento principal y lo agrega al final del documento de destino utilizando un salto de sección como separador.

Este método ignora laRemoveUnusedRegions opción.

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // A continuación se muestran dos formas de usar un DataTable como fuente de datos para una combinación de correspondencia.
    // 1: use la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento de origen de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## Execute(IDataReader) {#execute_4}

Realiza la combinación de correspondencia de IDataReader en el documento.

```csharp
public void Execute(IDataReader dataReader)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataReader | IDataReader | Fuente de datos para la operación de combinación de correspondencia. |

### Observaciones

Puedes pasar **SqlDataReader** o **OleDbDataReader** objeto en el método this como parámetro porque ambos implementaron **IDataReader** interfaz.

Tenga en cuenta que este método no usa regiones de combinación de correspondencia y para varios registros, el documento crecerá repitiendo todo el documento.

Este método ignora laRemoveUnusedRegions opción.

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia utilizando datos de un lector de datos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Product:\t");
builder.InsertField(" MERGEFIELD ProductName");
builder.Write("\nSupplier:\t");
builder.InsertField(" MERGEFIELD CompanyName");
builder.Writeln();
builder.InsertField(" MERGEFIELD QuantityPerUnit");
builder.Write(" for $");
builder.InsertField(" MERGEFIELD UnitPrice");

// Crear una cadena de conexión que apunte al archivo de base de datos "Northwind"
// en nuestro sistema de archivos local, abra una conexión y configure una consulta SQL.
string connectionString = @"Driver={Microsoft Access Driver (*.mdb)};Dbq=" + DatabaseDir + "Northwind.mdb";
string query = 
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, {fn ROUND(Products.UnitPrice,2)} as UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OdbcConnection connection = new OdbcConnection())
{
    connection.ConnectionString = connectionString;
    connection.Open();

    // Cree un comando SQL que generará datos para nuestra combinación de correspondencia.
    // Los nombres de las columnas de la tabla que devolverá esta sentencia SELECT
    // deberá corresponder a los campos de combinación que colocamos arriba.
    OdbcCommand command = connection.CreateCommand();
    command.CommandText = query;

    // Esto ejecutará el comando y almacenará los datos en el lector.
    OdbcDataReader reader = command.ExecuteReader(CommandBehavior.CloseConnection);

    // Tome los datos del lector y utilícelos en la combinación de correspondencia.
    doc.MailMerge.Execute(reader);
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## Execute(DataView) {#execute_3}

Realiza la combinación de correspondencia de un DataView en el documento.

```csharp
public void Execute(DataView dataView)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataView | DataView | Fuente de datos para la operación de combinación de correspondencia. |

### Observaciones

Este método es útil si recupera datos en un **Tabla de datos** pero luego necesita aplicar un filtro u ordenar antes de la combinación de correspondencia.

Tenga en cuenta que este método no usa regiones de combinación de correspondencia y para varios registros, el documento crecerá repitiendo todo el documento.

Este método ignora laRemoveUnusedRegions opción.

### Ejemplos

Muestra cómo editar datos de combinación de correspondencia con un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Cree una tabla de datos de la que nuestra combinación de correo obtendrá datos.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Podemos usar una vista de datos para modificar los datos de combinación de correo sin realizar cambios en la tabla de datos en sí.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Nuestra vista de datos ordena las entradas en orden descendente a lo largo de la columna "Grado"
// y filtra las filas con valores inferiores a 50 en esa columna.
// Tres de las cuatro filas se ajustan a esos criterios para que el documento de salida contenga tres documentos combinados.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## Execute(DataRow) {#execute_1}

Realiza la combinación de correspondencia de un DataRow en el documento.

```csharp
public void Execute(DataRow row)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| row | DataRow | Fila que contiene los datos que se insertarán en los campos de combinación de correspondencia. Los nombres de los campos no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |

### Observaciones

Utilice este método para completar los campos de combinación de correspondencia en el documento con valores de un **Fila de datos**.

Este método ignora laRemoveUnusedRegions opción.

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // A continuación se muestran dos formas de usar un DataTable como fuente de datos para una combinación de correspondencia.
    // 1: use la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento de origen de combinación de correspondencia.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
