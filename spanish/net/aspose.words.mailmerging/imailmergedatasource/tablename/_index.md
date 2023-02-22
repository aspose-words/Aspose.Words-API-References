---
title: IMailMergeDataSource.TableName
second_title: Referencia de API de Aspose.Words para .NET
description: IMailMergeDataSource propiedad. Devuelve el nombre de la fuente de datos.
type: docs
weight: 10
url: /es/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

Devuelve el nombre de la fuente de datos.

```csharp
public string TableName { get; }
```

### Valor_devuelto

El nombre de la fuente de datos. Cadena vacía si la fuente de datos no tiene nombre.

### Observaciones

Si está implementando[`IMailMergeDataSource`](../), devuelva el nombre de la fuente data de esta propiedad.

Aspose.Words usa este nombre para compararlo con el nombre de la región de combinación de correspondencia especificado en el documento de plantilla. La comparación entre el nombre del origen de datos y el nombre de la región de combinación de correspondencia no distingue entre mayúsculas y minúsculas.

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


