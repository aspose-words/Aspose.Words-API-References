---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words for .NET
description: IMailMergeDataSource GetChildDataSource method. The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region in C#.
type: docs
weight: 20
url: /net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

The Aspose.Words mail merge engine invokes this method when it encounters a beginning of a nested mail merge region.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tableName | String | The name of the mail merge region as specified in the template document. Case-insensitive. |

### Return Value

A data source object that will provide access to the data records of the specified table.

## Remarks

When the Aspose.Words mail merge engines populates a mail merge region with data and encounters the beginning of a nested mail merge region in the form of MERGEFIELD TableStart:TableName, it invokes `GetChildDataSource` on the current data source object. Your implementation needs to return a new data source object that will provide access to the child records of the current parent record. Aspose.Words will use the returned data source to populate the nested mail merge region.

Below are the rules that the implementation of `GetChildDataSource` must follow.

If the table that is represented by this data source object has a related child (detail) table with the specified name, then your implementation needs to return a new [`IMailMergeDataSource`](../) object that will provide access to the child records of the current record. An example of this is Orders / OrderDetails relationship. Let's assume that the current [`IMailMergeDataSource`](../) object represents the Orders table and it has a current order record. Next, Aspose.Words encounters "MERGEFIELD TableStart:OrderDetails" in the document and invokes `GetChildDataSource`. You need to create and return a [`IMailMergeDataSource`](../) object that will allow Aspose.Words to access the OrderDetails record for the current order.

If this data source object does not have a relation to the table with the specified name, then you need to return a [`IMailMergeDataSource`](../) object that will provide access to all records of the specified table.

If a table with the specified name does not exist, your implementation should return `null`.

## Examples

Shows how to execute a mail merge with a data source in the form of a custom object.

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

    // To use a custom object as a data source, it must implement the IMailMergeDataSource interface. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

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
