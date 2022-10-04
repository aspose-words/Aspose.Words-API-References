---
title: ExecuteWithRegions
second_title: Referencia de API de Aspose.Words para .NET
description: Realiza una combinación de correspondencia desde un origen de datos personalizado con regiones de combinación de correspondencia.
type: docs
weight: 200
url: /es/net/aspose.words.mailmerging/mailmerge/executewithregions/
---
## ExecuteWithRegions(IMailMergeDataSource) {#executewithregions}

Realiza una combinación de correspondencia desde un origen de datos personalizado con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(IMailMergeDataSource dataSource)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSource | IMailMergeDataSource | Un objeto que implementa la interfaz de fuente de datos de combinación de correspondencia personalizada. |

### Observaciones

Utilice este método para completar campos de combinación de correspondencia en el documento con valores de cualquier origen de datos personalizado, como un archivo XML o colecciones de objetos comerciales. Necesitas escribir tu propia clase que implementa el[`IMailMergeDataSource`](../../imailmergedatasource/) interfaz.

Puede utilizar este método sólo cuando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)es falso, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

### Ejemplos

Muestra cómo utilizar las regiones de combinación de correspondencia para ejecutar una combinación de correspondencia anidada.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, los MERGEFIELD contienen el nombre de una columna de una fuente de datos de combinación de correspondencia.
    // En su lugar, podemos usar los prefijos "TableStart:" y "TableEnd:" para comenzar/finalizar una región de combinación de correspondencia.
    // Cada región pertenecerá a una tabla con un nombre que coincida con la cadena inmediatamente después de los dos puntos del prefijo.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Estos MERGEFIELD están dentro de la región de combinación de correspondencia de la tabla "Clientes".
    // Cuando ejecutamos la combinación de correspondencia, este campo recibirá datos de filas en una fuente de datos llamada "Clientes".
    builder.Write("Full name:\t");
    builder.InsertField(" MERGEFIELD FullName ");
    builder.Write("\nAddress:\t");
    builder.InsertField(" MERGEFIELD Address ");
    builder.Write("\nOrders:\n");

    // Cree una segunda región de combinación de correo dentro de la región exterior para una fuente de datos llamada "Pedidos".
    // Las entradas de datos de "Pedidos" tienen una relación de muchos a uno con la fuente de datos de "Clientes".
    builder.InsertField(" MERGEFIELD TableStart:Orders");

    builder.Write("\tItem name:\t");
    builder.InsertField(" MERGEFIELD Name ");
    builder.Write("\n\tQuantity:\t");
    builder.InsertField(" MERGEFIELD Quantity ");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Cree datos relacionados con nombres que coincidan con los de nuestras regiones de combinación de correspondencia.
    CustomerList customers = new CustomerList();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    customers[0].Orders.Add(new Order("Rugby World Cup Cap", 2));
    customers[0].Orders.Add(new Order("Rugby World Cup Ball", 1));
    customers[1].Orders.Add(new Order("Rugby World Cup Guide", 1));

    // Para combinar correspondencia desde su fuente de datos, debemos envolverla en un objeto que implemente la interfaz IMailMergeDataSource.
    CustomerMailMergeDataSource customersDataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.ExecuteWithRegions(customersDataSource);

    doc.Save(ArtifactsDir + "NestedMailMergeCustom.CustomDataSource.docx");
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
        Orders = new List<Order>();
    }

    public string FullName { get; set; }
    public string Address { get; set; }
    public List<Order> Orders { get; set; }
}

/// <summary>
/// Un ejemplo de una colección tipada que contiene sus objetos de "datos".
/// </summary>
public class CustomerList : ArrayList
{
    public new Customer this[int index]
    {
        get { return (Customer) base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Un ejemplo de una clase secundaria de "entidad de datos" en su aplicación.
/// </summary>
public class Order
{
    public Order(string oName, int oQuantity)
    {
        Name = oName;
        Quantity = oQuantity;
    }

    public string Name { get; set; }
    public int Quantity { get; set; }
}

/// <summary>
/// Una fuente de datos de combinación de correspondencia personalizada que implementa para permitir Aspose.Words 
/// para combinar datos de sus objetos de Cliente en documentos de Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(CustomerList customers)
    {
        mCustomers = customers;

        // Cuando inicializamos la fuente de datos, su posición debe estar antes del primer registro.
        mRecordIndex = -1;
    }

    /// <summary>
    /// El nombre de la fuente de datos. Usado por Aspose.Words solo cuando se ejecuta la combinación de correspondencia con regiones repetibles.
    /// </summary>
    public string TableName
    {
        get { return "Customers"; }
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
            case "Order":
                fieldValue = mCustomers[mRecordIndex].Orders;
                return true;
            default:
                // Devuelve "falso" al motor de combinación de correspondencia de Aspose.Words para indicar
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
        switch (tableName)
        {
            // Obtenga la fuente de datos secundaria, cuyo nombre coincida con la región de combinación de correspondencia que usa sus columnas.
            case "Orders":
                return new OrderMailMergeDataSource(mCustomers[mRecordIndex].Orders);
            default:
                return null;
        }
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly CustomerList mCustomers;
    private int mRecordIndex;
}

public class OrderMailMergeDataSource : IMailMergeDataSource
{
    public OrderMailMergeDataSource(List<Order> orders)
    {
        mOrders = orders;

        // Cuando inicializamos la fuente de datos, su posición debe estar antes del primer registro.
        mRecordIndex = -1;
    }

    /// <summary>
    /// El nombre de la fuente de datos. Usado por Aspose.Words solo cuando se ejecuta la combinación de correspondencia con regiones repetibles.
    /// </summary>
    public string TableName
    {
        get { return "Orders"; }
    }

    /// <summary>
    /// Aspose.Words llama a este método para obtener un valor para cada campo de datos.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "Name":
                fieldValue = mOrders[mRecordIndex].Name;
                return true;
            case "Quantity":
                fieldValue = mOrders[mRecordIndex].Quantity;
                return true;
            default:
                // Devuelve "falso" al motor de combinación de correspondencia de Aspose.Words para indicar
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

    /// <summary>
    /// Devuelve nulo porque no tenemos elementos secundarios para este tipo de objeto.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mOrders.Count); }
    }

    private readonly List<Order> mOrders;
    private int mRecordIndex;
}
```

### Ver también

* interface [IMailMergeDataSource](../../imailmergedatasource/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(IMailMergeDataSourceRoot) {#executewithregions_1}

Realiza una combinación de correspondencia desde un origen de datos personalizado con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSourceRoot | IMailMergeDataSourceRoot | Un objeto que implementa la interfaz raíz de origen de datos de combinación de correspondencia personalizada. |

### Observaciones

Utilice este método para completar campos de combinación de correspondencia en el documento con valores de cualquier origen de datos personalizado, como un archivo XML o colecciones de objetos comerciales. Necesita escribir sus propias clases que implementen el[`IMailMergeDataSourceRoot`](../../imailmergedatasourceroot/) y[`IMailMergeDataSource`](../../imailmergedatasource/) interfaces

Puede utilizar este método sólo cuando[`IsBidiTextSupportedOnUpdate`](../../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/)es falso, es decir, no necesita compatibilidad con idiomas de derecha a izquierda (como árabe o hebreo).

### Ejemplos

Realiza la combinación de correo desde una fuente de datos personalizada con datos maestro-detalle.

```csharp
public void CustomDataSourceRoot()
{
    // Cree un documento con dos regiones de combinación de correspondencia denominadas "Washington" y "Seattle".
    string[] mailMergeRegions = { "Vancouver", "Seattle" };
    Document doc = CreateSourceDocumentWithMailMergeRegions(mailMergeRegions);

    // Crear dos fuentes de datos para la combinación de correspondencia.
    EmployeeList employeesWashingtonBranch = new EmployeeList();
    employeesWashingtonBranch.Add(new Employee("John Doe", "Sales"));
    employeesWashingtonBranch.Add(new Employee("Jane Doe", "Management"));

    EmployeeList employeesSeattleBranch = new EmployeeList();
    employeesSeattleBranch.Add(new Employee("John Cardholder", "Management"));
    employeesSeattleBranch.Add(new Employee("Joe Bloggs", "Sales"));

    // Registrar nuestras fuentes de datos por nombre en una raíz de fuente de datos.
    // Si estamos a punto de usar esta fuente de datos raíz en una combinación de correo con regiones,
    // el nombre registrado de cada origen debe coincidir con el nombre de una región de combinación de correspondencia existente en el documento de origen de combinación de correspondencia.
    DataSourceRoot sourceRoot = new DataSourceRoot();
    sourceRoot.RegisterSource(mailMergeRegions[0], new EmployeeListMailMergeSource(employeesWashingtonBranch));
    sourceRoot.RegisterSource(mailMergeRegions[1], new EmployeeListMailMergeSource(employeesSeattleBranch));

    // Dado que tenemos regiones de combinación de correspondencia consecutivas, normalmente tendríamos que realizar dos combinaciones de correspondencia.
    // Sin embargo, una fuente de combinación de correo con una raíz de datos puede completar varias regiones
    // si la raíz contiene tablas con los nombres/nombres de columna correspondientes.
    doc.MailMerge.ExecuteWithRegions(sourceRoot);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSourceRoot.docx");
}

/// <summary>
/// Cree un documento que contenga regiones de combinación de correspondencia consecutivas, con nombres designados por la matriz de entrada,
/// para una tabla de datos de empleados.
/// </summary>
private static Document CreateSourceDocumentWithMailMergeRegions(string[] regions)
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    foreach (string s in regions)
    {
        builder.Writeln("\n" + s + " branch: ");
        builder.InsertField(" MERGEFIELD TableStart:" + s);
        builder.InsertField(" MERGEFIELD FullName");
        builder.Write(", ");
        builder.InsertField(" MERGEFIELD Department");
        builder.InsertField(" MERGEFIELD TableEnd:" + s);
    }

    return doc;
}

/// <summary>
/// Un ejemplo de una clase de "entidad de datos" en su aplicación.
/// </summary>
private class Employee
{
    public Employee(string aFullName, string aDepartment)
    {
        FullName = aFullName;
        Department = aDepartment;
    }

    public string FullName { get; }
    public string Department { get; }
}

/// <summary>
/// Un ejemplo de una colección tipada que contiene sus objetos de "datos".
/// </summary>
private class EmployeeList : ArrayList
{
    public new Employee this[int index]
    {
        get { return (Employee)base[index]; }
        set { base[index] = value; }
    }
}

/// <summary>
/// Raíz de la fuente de datos que se puede pasar directamente a una combinación de correspondencia que puede registrar y contener muchas fuentes de datos secundarias.
/// Todas estas fuentes deben implementar IMailMergeDataSource, y están registradas y diferenciadas por un nombre
/// que corresponde a una región de combinación de correo que leerá los datos respectivos.
/// </summary>
private class DataSourceRoot : IMailMergeDataSourceRoot
{
    public IMailMergeDataSource GetDataSource(string tableName)
    {
        EmployeeListMailMergeSource source = mSources[tableName];
        source.Reset();
        return mSources[tableName];
    }

    public void RegisterSource(string sourceName, EmployeeListMailMergeSource source)
    {
        mSources.Add(sourceName, source);
    }

    private readonly Dictionary<string, EmployeeListMailMergeSource> mSources = new Dictionary<string, EmployeeListMailMergeSource>();
}

/// <summary>
/// Fuente de datos de combinación de correspondencia personalizada.
/// </summary>
private class EmployeeListMailMergeSource : IMailMergeDataSource
{
    public EmployeeListMailMergeSource(EmployeeList employees)
    {
        mEmployees = employees;
        mRecordIndex = -1;
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

    private bool IsEof
    {
        get { return (mRecordIndex >= mEmployees.Count); }
    }

    public void Reset()
    {
        mRecordIndex = -1;
    }

    /// <summary>
    /// El nombre de la fuente de datos. Usado por Aspose.Words solo cuando se ejecuta la combinación de correspondencia con regiones repetibles.
    /// </summary>
    public string TableName
    {
        get { return "Employees"; }
    }

    /// <summary>
    /// Aspose.Words llama a este método para obtener un valor para cada campo de datos.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mEmployees[mRecordIndex].FullName;
                return true;
            case "Department":
                fieldValue = mEmployees[mRecordIndex].Department;
                return true;
            default:
                // Devuelve "falso" al motor de combinación de correspondencia de Aspose.Words para indicar
                // que no pudimos encontrar un campo con este nombre.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Las fuentes de datos secundarias son para combinaciones de correspondencia anidadas.
    /// </summary>
    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        throw new System.NotImplementedException();
    }

    private readonly EmployeeList mEmployees;
    private int mRecordIndex;
}
```

### Ver también

* interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataSet) {#executewithregions_2}

Realiza la combinación de correspondencia de un conjunto de datos en un documento con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(DataSet dataSet)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataSet | DataSet | DataSet que contiene datos que se insertarán en los campos de combinación de correspondencia. |

### Observaciones

Utilice este método para realizar la combinación de correspondencia desde una o más tablas en regiones de combinación mail repetibles en el documento. Las regiones de combinación de correspondencia dentro del documento crecerán dinámicamente para acomodar registros en las tablas correspondientes.

Cada tabla en el DataSet debe tener un nombre.

El documento debe tener regiones de combinación de correspondencia definidas con nombres que hagan referencia a las tablas en el conjunto de datos.

Para especificar una región de combinación de correspondencia en el documento, debe insertar dos campos de combinación de correspondencia para marcar el comienzo y el final de la región de combinación de correspondencia.

Todo el contenido del documento que se incluye dentro de una región de combinación de correo se repetirá automáticamente para cada registro en DataTable.

Para marcar el comienzo de una región de combinación de correspondencia, inserte un MERGEFIELD con el nombre TableStart:MyTable, donde MyTable corresponde a uno de los nombres de tabla en su DataSet.

Para marcar el final de la región de combinación de correspondencia, inserte otro MERGEFIELD con el nombre TableEnd:MyTable.

Para insertar un MERGEFIELD en Word, use el comando Insertar/Campo y seleccione MergeField y luego escriba el nombre del campo.

Los campos TableStart y TableEnd deben estar dentro de la misma sección en su documento.

Si se usa dentro de una tabla, TableStart y TableEnd deben estar dentro de la misma fila en la tabla.

Las regiones de combinación de correspondencia en un documento deben estar bien formadas (siempre es necesario que haya un par de campos combinados TableStart y TableEnd coincidentes con el mismo nombre de tabla).

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia anidada con dos regiones de combinación y dos tablas de datos.

```csharp
[Test]
public void ExecuteWithRegionsNested()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Normalmente, los MERGEFIELD contienen el nombre de una columna de una fuente de datos de combinación de correspondencia.
    // En su lugar, podemos usar los prefijos "TableStart:" y "TableEnd:" para comenzar/finalizar una región de combinación de correspondencia.
    // Cada región pertenecerá a una tabla con un nombre que coincida con la cadena inmediatamente después de los dos puntos del prefijo.
    builder.InsertField(" MERGEFIELD TableStart:Customers");

    // Este MERGEFIELD está dentro de la región de combinación de correspondencia de la tabla "Clientes".
    // Cuando ejecutamos la combinación de correspondencia, este campo recibirá datos de filas en una fuente de datos llamada "Clientes".
    builder.Write("Orders for ");
    builder.InsertField(" MERGEFIELD CustomerName");
    builder.Write(":");

    // Crear encabezados de columna para una tabla que contendrá valores de una segunda región interna.
    builder.StartTable();
    builder.InsertCell();
    builder.Write("Item");
    builder.InsertCell();
    builder.Write("Quantity");
    builder.EndRow();

    // Cree una segunda región de combinación de correo dentro de la región exterior para una tabla denominada "Pedidos".
    // La tabla "Pedidos" tiene una relación de varios a uno con la tabla "Clientes" en la columna "CustomerID".
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD TableStart:Orders");
    builder.InsertField(" MERGEFIELD ItemName");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD Quantity");

    // Finaliza la región interior y luego finaliza la región exterior. La apertura y cierre de una región de combinación de correspondencia debe
    // ocurre en la misma fila de una tabla.
    builder.InsertField(" MERGEFIELD TableEnd:Orders");
    builder.EndTable();

    builder.InsertField(" MERGEFIELD TableEnd:Customers");

    // Cree un conjunto de datos que contenga las dos tablas con los nombres y relaciones requeridos.
    // Cada documento de combinación para cada fila de la tabla "Clientes" de la región de combinación externa realizará su combinación de correspondencia en la tabla "Pedidos".
    // Cada documento combinado mostrará todas las filas de la última tabla cuyos valores de columna "CustomerID" coincidan con la fila actual de la tabla "Clientes".
    DataSet customersAndOrders = CreateDataSet();
    doc.MailMerge.ExecuteWithRegions(customersAndOrders);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsNested.docx");
}

/// <summary>
/// Genera un conjunto de datos que tiene dos tablas de datos denominadas "Clientes" y "Pedidos", con una relación de uno a varios en la columna "CustomerID".
/// </summary>
private static DataSet CreateDataSet()
{
    DataTable tableCustomers = new DataTable("Customers");
    tableCustomers.Columns.Add("CustomerID");
    tableCustomers.Columns.Add("CustomerName");
    tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
    tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

    DataTable tableOrders = new DataTable("Orders");
    tableOrders.Columns.Add("CustomerID");
    tableOrders.Columns.Add("ItemName");
    tableOrders.Columns.Add("Quantity");
    tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
    tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
    tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

    DataSet dataSet = new DataSet();
    dataSet.Tables.Add(tableCustomers);
    dataSet.Tables.Add(tableOrders);
    dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

    return dataSet;
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataTable) {#executewithregions_3}

Realiza la combinación de correspondencia de un DataTable en el documento con las regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(DataTable dataTable)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataTable | DataTable | Fuente de datos para la operación de combinación de correspondencia. La tabla debe tener su **Nombre de la tabla** conjunto de propiedades |

### Observaciones

El documento debe tener una región de combinación de correspondencia definida con un nombre que coincida con  **DataTable.TableName**.

Si hay otras regiones de combinación de correspondencia definidas en el documento, se dejan intactas. Esto permite realizar varias operaciones de combinación de correspondencia.

### Ejemplos

Muestra cómo formatear celdas durante una combinación de correspondencia.

```csharp
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind suppliers.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldAlternatingRows();

    DataTable dataTable = GetSuppliersDataTable();
    doc.MailMerge.ExecuteWithRegions(dataTable);

    doc.Save(ArtifactsDir + "MailMergeEvent.AlternatingRows.docx");

/// <summary>
/// Da formato a las filas de la tabla a medida que se lleva a cabo una combinación de correspondencia para alternar entre dos colores en filas pares/impares.
/// </summary>
private class HandleMergeFieldAlternatingRows : IFieldMergingCallback
{
    /// <summary>
    /// Llamado cuando una combinación de correo combina datos en un MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (mBuilder == null)
            mBuilder = new DocumentBuilder(args.Document);

        // Esto es cierto si estamos en la primera columna, lo que significa que nos hemos movido a una nueva fila.
        if (args.FieldName == "CompanyName")
        {
            Color rowColor = IsOdd(mRowIdx) ? Color.FromArgb(213, 227, 235) : Color.FromArgb(242, 242, 242);

            for (int colIdx = 0; colIdx < 4; colIdx++)
            {
                mBuilder.MoveToCell(0, mRowIdx, colIdx, 0);
                mBuilder.CellFormat.Shading.BackgroundPatternColor = rowColor;
            }

            mRowIdx++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Hacer nada.
    }

    private DocumentBuilder mBuilder;
    private int mRowIdx;
}

/// <summary>
/// Función necesaria para la autoportación de Visual Basic que devuelve la paridad del número pasado.
/// </summary>
private static bool IsOdd(int value)
{
    return (value / 2 * 2).Equals(value);
}

/// <summary>
/// Crea una fuente de datos de combinación de correspondencia.
/// </summary>
private static DataTable GetSuppliersDataTable()
{
    DataTable dataTable = new DataTable("Suppliers");
    dataTable.Columns.Add("CompanyName");
    dataTable.Columns.Add("ContactName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Company " + i;
        datarow[1] = "Contact " + i;
    }

    return dataTable;
}
```

Muestra cómo usar regiones para ejecutar dos combinaciones de correo separadas en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si queremos realizar dos fusiones de correo consecutivas en un documento mientras tomamos datos de dos tablas
// relacionados entre sí de alguna manera, podemos separar las fusiones de correo con las regiones.
// Normalmente, los MERGEFIELD contienen el nombre de una columna de una fuente de datos de combinación de correspondencia.
// En su lugar, podemos usar los prefijos "TableStart:" y "TableEnd:" para comenzar/finalizar una región de combinación de correspondencia.
// Cada región pertenecerá a una tabla con un nombre que coincida con la cadena inmediatamente después de los dos puntos del prefijo.
// Estas regiones están separadas para datos no relacionados, mientras que pueden anidarse para datos jerárquicos.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Ambos MERGEFIELD se refieren al mismo nombre de columna, pero los valores de cada uno provendrán de diferentes tablas de datos.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crear dos tablas de datos no relacionadas.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Tendremos que ejecutar una combinación de correspondencia por tabla. La primera combinación de correspondencia llenará los MERGEFIELDs
// en el rango "Ciudades" dejando los campos del rango "Frutas" sin llenar.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Ejecute una segunda combinación para la tabla "Fruit", mientras usa una vista de datos
// para ordenar las filas en orden ascendente en la columna "Nombre" antes de la fusión.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(DataView) {#executewithregions_4}

Realiza la combinación de correspondencia desde un DataView en el documento con regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(DataView dataView)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataView | DataView | Fuente de datos para la operación de combinación de correspondencia. La fuente table del **vista de datos** debe tener su **Nombre de la tabla** conjunto de propiedades |

### Observaciones

Este método es útil si recupera datos en un **Tabla de datos** pero luego necesita aplicar un filtro u ordenar antes de la combinación de correspondencia.

El documento debe tener una región de combinación de correspondencia definida con un nombre que coincida con  **DataView.Table.TableName**.

Si hay otras regiones de combinación de correspondencia definidas en el documento, se dejan intactas. Esto permite realizar varias operaciones de combinación de correspondencia.

### Ejemplos

Muestra cómo usar regiones para ejecutar dos combinaciones de correo separadas en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si queremos realizar dos fusiones de correo consecutivas en un documento mientras tomamos datos de dos tablas
// relacionados entre sí de alguna manera, podemos separar las fusiones de correo con las regiones.
// Normalmente, los MERGEFIELD contienen el nombre de una columna de una fuente de datos de combinación de correspondencia.
// En su lugar, podemos usar los prefijos "TableStart:" y "TableEnd:" para comenzar/finalizar una región de combinación de correspondencia.
// Cada región pertenecerá a una tabla con un nombre que coincida con la cadena inmediatamente después de los dos puntos del prefijo.
// Estas regiones están separadas para datos no relacionados, mientras que pueden anidarse para datos jerárquicos.
builder.Writeln("\tCities: ");
builder.InsertField(" MERGEFIELD TableStart:Cities");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Cities");
builder.InsertParagraph();

// Ambos MERGEFIELD se refieren al mismo nombre de columna, pero los valores de cada uno provendrán de diferentes tablas de datos.
builder.Writeln("\tFruit: ");
builder.InsertField(" MERGEFIELD TableStart:Fruit");
builder.InsertField(" MERGEFIELD Name");
builder.InsertField(" MERGEFIELD TableEnd:Fruit");

// Crear dos tablas de datos no relacionadas.
DataTable tableCities = new DataTable("Cities");
tableCities.Columns.Add("Name");
tableCities.Rows.Add(new object[] { "Washington" });
tableCities.Rows.Add(new object[] { "London" });
tableCities.Rows.Add(new object[] { "New York" });

DataTable tableFruit = new DataTable("Fruit");
tableFruit.Columns.Add("Name");
tableFruit.Rows.Add(new object[] { "Cherry" });
tableFruit.Rows.Add(new object[] { "Apple" });
tableFruit.Rows.Add(new object[] { "Watermelon" });
tableFruit.Rows.Add(new object[] { "Banana" });

// Tendremos que ejecutar una combinación de correspondencia por tabla. La primera combinación de correspondencia llenará los MERGEFIELDs
// en el rango "Ciudades" dejando los campos del rango "Frutas" sin llenar.
doc.MailMerge.ExecuteWithRegions(tableCities);

// Ejecute una segunda combinación para la tabla "Fruit", mientras usa una vista de datos
// para ordenar las filas en orden ascendente en la columna "Nombre" antes de la fusión.
DataView dv = new DataView(tableFruit);
dv.Sort = "Name ASC";
doc.MailMerge.ExecuteWithRegions(dv);

doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsConcurrent.docx");
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

---

## ExecuteWithRegions(IDataReader, string) {#executewithregions_5}

Realiza la combinación de correspondencia de IDataReader en el documento con las regiones de combinación de correspondencia.

```csharp
public void ExecuteWithRegions(IDataReader dataReader, string tableName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dataReader | IDataReader | Origen de los registros de datos para la combinación de correspondencia como OleDbDataReader o SqlDataReader. |
| tableName | String | Nombre de la región de combinación de correspondencia en el documento para completar. |

### Observaciones

Puedes pasar **SqlDataReader** o **OleDbDataReader** objeto en el método this como parámetro porque ambos implementaron **IDataReader** interfaz.

### Ejemplos

Muestra cómo insertar imágenes almacenadas en un campo BLOB de base de datos en un informe.

```csharp
public void ImageFromBlob()
{
    Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

    doc.MailMerge.FieldMergingCallback = new HandleMergeImageFieldFromBlob();

    string connString = $"Provider=Microsoft.Jet.OLEDB.4.0;Data Source={DatabaseDir + "Northwind.mdb"};";
    string query = "SELECT FirstName, LastName, Title, Address, City, Region, Country, PhotoBLOB FROM Employees";

    using (OleDbConnection conn = new OleDbConnection(connString))
    {
        conn.Open();

        // Abra el lector de datos, que debe estar en un modo que lea todos los registros a la vez.
        OleDbCommand cmd = new OleDbCommand(query, conn);
        IDataReader dataReader = cmd.ExecuteReader();

        doc.MailMerge.ExecuteWithRegions(dataReader, "Employees");
    }

    doc.Save(ArtifactsDir + "MailMergeEvent.ImageFromBlob.docx");

private class HandleMergeImageFieldFromBlob : IFieldMergingCallback
{
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        // Hacer nada.
    }

    /// <summary>
    /// Esto se llama cuando una combinación de correspondencia encuentra un MERGEFIELD en el documento con una etiqueta "Imagen:" en su nombre.
    /// </summary>
    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        MemoryStream imageStream = new MemoryStream((byte[])e.FieldValue);
        e.ImageStream = imageStream;
    }
}
```

### Ver también

* class [MailMerge](../)
* espacio de nombres [Aspose.Words.MailMerging](../../mailmerge/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
