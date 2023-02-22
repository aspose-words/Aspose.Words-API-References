---
title: IMailMergeDataSource.GetChildDataSource
second_title: Referencia de API de Aspose.Words para .NET
description: IMailMergeDataSource método. El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el comienzo de una región de combinación de correspondencia anidada.
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

El motor de combinación de correspondencia de Aspose.Words invoca este método cuando encuentra el comienzo de una región de combinación de correspondencia anidada.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| tableName | String | El nombre de la región de combinación de correspondencia como se especifica en el documento de plantilla. No distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

Un objeto de origen de datos que proporcionará acceso a los registros de datos de la tabla especificada.

### Observaciones

Cuando los motores de combinación de correspondencia de Aspose.Words llenan una región de combinación de correspondencia con datos y encuentra el comienzo de una región de combinación de correspondencia anidada en forma de MERGEFIELD TableStart:TableName, invoca`GetChildDataSource` en el objeto de origen de datos current . Su implementación debe devolver un nuevo objeto de origen de datos que proporcione acceso a los registros child del registro principal actual. Aspose.Words utilizará la fuente de datos devuelta para completar la región de combinación de correspondencia anidada.

A continuación se encuentran las reglas que la implementación de`GetChildDataSource` debe seguir.

Si la tabla que está representada por este objeto de fuente de datos tiene una tabla secundaria relacionada (detalle) con el nombre especificado, entonces su implementación necesita devolver una nueva[`IMailMergeDataSource`](../) objeto que proporcionará access a los registros secundarios del registro actual. Un ejemplo de esto es la relación Orders / OrderDetails. Supongamos que la corriente[`IMailMergeDataSource`](../) object representa la tabla Pedidos y tiene un registro de pedido actual. A continuación, Aspose.Words encuentra "MERGEFIELD TableStart:OrderDetails" en el documento e invoca`GetChildDataSource` . Necesitas crear y devolver un[`IMailMergeDataSource`](../) objeto que permitirá a Aspose.Words acceder al registro OrderDetails para el pedido actual.

Si este objeto de origen de datos no tiene una relación con la tabla con el nombre especificado, debe devolver a[`IMailMergeDataSource`](../)objeto que proporcionará acceso a todos los registros de la tabla especificada.

Si no existe una tabla con el nombre especificado, su implementación debería devolver`nulo` .

### Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de un objeto personalizado.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    // Para usar un objeto personalizado como fuente de datos, debe implementar la interfaz IMailMergeDataSource. 
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
/// Una fuente de datos de combinación de correspondencia personalizada que implementa para permitir Aspose.Words 
/// para combinar datos de sus objetos de Cliente en documentos de Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
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

* interface [IMailMergeDataSource](../)
* espacio de nombres [Aspose.Words.MailMerging](../../imailmergedatasource/)
* asamblea [Aspose.Words](../../../)


