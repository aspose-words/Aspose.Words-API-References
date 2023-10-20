---
title: IMailMergeDataSource Interface
linktitle: IMailMergeDataSource
articleTitle: IMailMergeDataSource
second_title: Aspose.Words para .NET
description: Aspose.Words.MailMerging.IMailMergeDataSource interfaz. Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada como una lista de objetos. También se admiten datos maestrodetalle en C#.
type: docs
weight: 3810
url: /es/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Implemente esta interfaz para permitir la combinación de correspondencia desde una fuente de datos personalizada, como una lista de objetos. También se admiten datos maestro-detalle.

```csharp
public interface IMailMergeDataSource
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Devuelve el nombre de la fuente de datos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(*string*) | El motor de combinación de correspondencia Aspose.Words invoca este método cuando encuentra el comienzo de una región de combinación de correspondencia anidada. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(*string, out object*) | Devuelve un valor para el nombre de campo especificado o`FALSO` si no se encuentra el campo. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Avanza al siguiente registro en la fuente de datos. |

## Observaciones

Cuando se crea una fuente de datos, se debe inicializar para que apunte a BOF (antes del primer registro). El motor de combinación de correspondencia Aspose.Words invocará[`MoveNext`](./movenext/) para avanzar al siguiente registro y luego invocar[`GetValue`](./getvalue/) para cada campo de combinación que encuentre en el documento o en la región de combinación de correspondencia actual.

## Ejemplos

Muestra cómo ejecutar una combinación de correspondencia con una fuente de datos en forma de objeto personalizado.

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
 /// Una fuente de datos de combinación de correspondencia personalizada que implementas para permitir Aspose.Words
/// para combinar datos de correspondencia de sus objetos de Cliente en documentos de Microsoft Word.
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
    /// El nombre de la fuente de datos. Utilizado por Aspose.Words solo cuando se ejecuta combinación de correspondencia con regiones repetibles.
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
    /// Una implementación estándar para pasar al siguiente registro de una colección.
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

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
