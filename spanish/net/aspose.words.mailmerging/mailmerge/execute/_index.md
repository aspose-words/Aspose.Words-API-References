---
title: MailMerge.Execute
linktitle: Execute
articleTitle: Execute
second_title: Aspose.Words para .NET
description: Optimice su proceso de envío de correo con el método MailMerge Execute, que combina sin esfuerzo datos de fuentes personalizadas para una comunicación personalizada.
type: docs
weight: 180
url: /es/net/aspose.words.mailmerging/mailmerge/execute/
---
## Execute(*[IMailMergeDataSource](../../imailmergedatasource/)*) {#execute}

Realiza una combinación de correspondencia desde una fuente de datos personalizada.

```csharp
public void Execute(IMailMergeDataSource dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un objeto que implementa la interfaz de fuente de datos de combinación de correspondencia personalizada. |

## Observaciones

Utilice este método para rellenar los campos de combinación de correspondencia del documento con valores de cualquier fuente de datos, como una lista, una tabla hash o algún objeto. Debe escribir su propia clase que implemente el método.[`IMailMergeDataSource`](../../imailmergedatasource/) interfaz.

Puedes utilizar este método sólo cuando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) es`FALSO`, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de un objeto personalizado.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // Para utilizar un objeto personalizado como fuente de datos, debe implementar la interfaz IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Un ejemplo de una clase de "entidad de datos" en su aplicación.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// Una fuente de datos de combinación de correspondencia personalizada que se implementa para permitir Aspose.Words
/// para combinar datos de sus objetos de Cliente en documentos de Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Cuando inicializamos la fuente de datos, su posición debe ser anterior al primer registro.
        mRecordIndex = -1;
    }

    /// <summary>
    /// El nombre de la fuente de datos. Aspose.Words lo utiliza solo al ejecutar la combinación de correspondencia con regiones repetibles.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words llama a este método para obtener un valor para cada campo de datos.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // Devuelve "falso" al motor de combinación de correspondencia Aspose.Words para indicar
                // que no pudimos encontrar un campo con este nombre.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Una implementación estándar para pasar al siguiente registro en una colección.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Ver también

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

---

## Execute(*string[], object[]*) {#execute_5}

Realiza una operación de combinación de correspondencia para un solo registro.

```csharp
public void Execute(string[] fieldNames, object[] values)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fieldNames | String[] | Matriz de nombres de campos de combinación. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |
| values | Object[] | Matriz de valores que se insertarán en los campos de combinación. El número de elementos en esta matriz debe ser el mismo que el número de elementos en*fieldNames*. |

## Observaciones

Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de una matriz de objetos.

Este método fusiona los datos de un solo registro. La matriz de nombres de campo y la matriz de valores representan los datos de un solo registro.

Este método no utiliza regiones de combinación de correspondencia.

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

Muestra cómo fusionar una imagen de una URI como datos de combinación de correspondencia en un MERGEFIELD.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos MERGEFIELD con etiquetas "Image:" recibirán una imagen durante una combinación de correspondencia.
// La cadena después de los dos puntos en la etiqueta "Imagen:" corresponde a un nombre de columna
// en la fuente de datos cuyas celdas contienen URI de archivos de imagen.
builder.InsertField("MERGEFIELD  Image:logo_FromWeb ");
builder.InsertField("MERGEFIELD  Image:logo_FromFileSystem ");

 // Crea una fuente de datos que contenga las URI de las imágenes que fusionaremos.
// Una URI puede ser una URL web que apunta a una imagen o un nombre de archivo del sistema de archivos local de un archivo de imagen.
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
//Se lanza porque HttpResponse es nulo en la prueba.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

Necesitaremos cerrar esta respuesta manualmente para asegurarnos de no agregar ningún contenido superfluo al documento después de guardarlo.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

---

## Execute(*DataTable*) {#execute_2}

Realiza la fusión de correspondencia desde un DataTable al documento.

```csharp
public void Execute(DataTable table)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| table | DataTable | Tabla que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |

## Observaciones

Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de a **Tabla de datos**.

Todos los registros de la tabla se fusionan en el documento.

Puede utilizar el campo SIGUIENTE en el documento de Word para provocar[`MailMerge`](../) objeto para seleccionar el siguiente registro del**Tabla de datos** y continuar fusionando. Esto se puede utilizar al crear documentos como etiquetas de correo.

Cuando[`MailMerge`](../) El objeto llega al final del documento principal y todavía hay más filas en el**Tabla de datos**copia todo el contenido del documento principal y lo agrega al final del documento de destino usando un salto de sección como separador.

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    A continuación se muestran dos formas de utilizar una DataTable como fuente de datos para una combinación de correspondencia.
    // 1 - Utilice la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento fuente de combinación de correspondencia.
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
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

---

## Execute(*IDataReader*) {#execute_4}

Realiza la combinación de correspondencia desde**Lector de datos IDataReader** en el documento.

```csharp
public void Execute(IDataReader dataReader)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataReader | IDataReader | Fuente de datos para la operación de combinación de correspondencia. |

## Observaciones

Puedes pasar**Lector de datos SQL** o**Lector de datos OleDb**objeto en el método this como parámetro porque ambos lo implementaron**Lector de datos IDataReader** interfaz.

Tenga en cuenta que este método no utiliza regiones de combinación de correspondencia y, para varios registros, el documento the crecerá repitiendo todo el documento.

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

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

// Crea una cadena de conexión que apunta al archivo de base de datos "Northwind"
// en nuestro sistema de archivos local, abra una conexión y configure una consulta SQL.
string connectionString = @"Provider = Microsoft.ACE.OLEDB.12.0; Data Source=" + DatabaseDir + "Northwind.accdb";
string query =
    @"SELECT Products.ProductName, Suppliers.CompanyName, Products.QuantityPerUnit, Products.UnitPrice
    FROM Products 
    INNER JOIN Suppliers 
    ON Products.SupplierID = Suppliers.SupplierID";

using (OleDbConnection connection = new OleDbConnection(connectionString))
{
    // Cree un comando SQL que obtendrá datos para nuestra combinación de correspondencia.
    // Los nombres de las columnas de la tabla que devolverá esta declaración SELECT
    // deberá corresponder a los campos de combinación que colocamos arriba.
    OleDbCommand command = new OleDbCommand(query, connection);
    command.CommandText = query;
    try
    {
        connection.Open();
        using (OleDbDataReader reader = command.ExecuteReader())
        {
            //Toma los datos del lector y úsalos en la combinación de correspondencia.
            doc.MailMerge.Execute(reader);
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine(ex.Message);
    }
}

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataReader.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

---

## Execute(*DataView*) {#execute_3}

Realiza la combinación de correspondencia desde un**Vista de datos** en el documento.

```csharp
public void Execute(DataView dataView)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataView | DataView | Fuente de datos para la operación de combinación de correspondencia. |

## Observaciones

Este método es útil si recupera datos en un**Tabla de datos** pero entonces es necesario aplicar un filtro o clasificación antes de combinar la correspondencia.

Tenga en cuenta que este método no utiliza regiones de combinación de correspondencia y, para varios registros, el documento the crecerá repitiendo todo el documento.

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

Muestra cómo editar datos de combinación de correspondencia con un DataView.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Congratulations ");
builder.InsertField(" MERGEFIELD Name");
builder.Write(" for passing with a grade of ");
builder.InsertField(" MERGEFIELD Grade");

// Cree una tabla de datos de la cual nuestra combinación de correspondencia obtendrá los datos.
DataTable table = new DataTable("ExamResults");
table.Columns.Add("Name");
table.Columns.Add("Grade");
table.Rows.Add(new object[] { "John Doe", "67" });
table.Rows.Add(new object[] { "Jane Doe", "81" });
table.Rows.Add(new object[] { "John Cardholder", "47" });
table.Rows.Add(new object[] { "Joe Bloggs", "75" });

// Podemos utilizar una vista de datos para alterar los datos de combinación de correspondencia sin realizar cambios en la tabla de datos en sí.
DataView view = new DataView(table);
view.Sort = "Grade DESC";
view.RowFilter = "Grade >= 50";

// Nuestra vista de datos ordena las entradas en orden descendente a lo largo de la columna "Calificación"
// y filtra las filas con valores menores a 50 en esa columna.
// Tres de las cuatro filas cumplen esos criterios, por lo que el documento de salida contendrá tres documentos combinados.
doc.MailMerge.Execute(view);

doc.Save(ArtifactsDir + "MailMerge.ExecuteDataView.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)

---

## Execute(*DataRow*) {#execute_1}

Realiza la combinación de correspondencia desde un**Fila de datos** en el documento.

```csharp
public void Execute(DataRow row)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| row | DataRow | Fila que contiene datos que se insertarán en los campos de combinación de correspondencia. Los nombres de campo no distinguen entre mayúsculas y minúsculas. Si se encuentra un nombre de campo que no se encuentra en el documento, se ignora. |

## Observaciones

Utilice este método para rellenar los campos de combinación de correspondencia en el documento con valores de un**Fila de datos**.

Este método ignora elRemoveUnusedRegions opción.

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con datos de una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    A continuación se muestran dos formas de utilizar una DataTable como fuente de datos para una combinación de correspondencia.
    // 1 - Utilice la tabla completa para la combinación de correspondencia para crear un documento de combinación de correspondencia de salida para cada fila de la tabla:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilice una fila de la tabla para crear un documento de combinación de correspondencia de salida:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento fuente de combinación de correspondencia.
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
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
