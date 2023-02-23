---
title: IMailMergeDataSource.GetValue
linktitle: GetValue
second_title: Aspose.Words for .NET API Reference
description: IMailMergeDataSource method. Returns a value for the specified field name or false if the field is not found in C#.
type: docs
weight: 30
url: /net/aspose.words.mailmerging/imailmergedatasource/getvalue/
---
## IMailMergeDataSource.GetValue method

Returns a value for the specified field name or `false` if the field is not found.

```csharp
public bool GetValue(string fieldName, out object fieldValue)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldName | String | The name of the data field. |
| fieldValue | Object& | Returns the field value. |

### Return Value

`true` if value was found.

## Examples

Shows how to execute a mail merge with a data source in the form of a custom object.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

    // To use a custom object as a data source, it must implement the IMailMergeDataSource interface. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");

/// <summary>
/// An example of a "data entity" class in your application.
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
/// A custom mail merge data source that you implement to allow Aspose.Words 
/// to mail merge data from your Customer objects into Microsoft Word documents.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // When we initialize the data source, its position must be before the first record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// The name of the data source. Used by Aspose.Words only when executing mail merge with repeatable regions.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words calls this method to get a value for every data field.
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
                // Return "false" to the Aspose.Words mail merge engine to signify
                // that we could not find a field with this name.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// A standard implementation for moving to a next record in a collection.
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

### See Also

* interface [IMailMergeDataSource](../)
* namespace [Aspose.Words.MailMerging](../../imailmergedatasource/)
* assembly [Aspose.Words](../../../)
