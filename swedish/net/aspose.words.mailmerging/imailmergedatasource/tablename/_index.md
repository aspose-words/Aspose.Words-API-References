---
title: IMailMergeDataSource.TableName
second_title: Aspose.Words för .NET API Referens
description: IMailMergeDataSource fast egendom. Returnerar namnet på datakällan.
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/imailmergedatasource/tablename/
---
## IMailMergeDataSource.TableName property

Returnerar namnet på datakällan.

```csharp
public string TableName { get; }
```

### Returvärde

Namnet på datakällan. Tom sträng om datakällan inte har något namn.

### Anmärkningar

Om du implementerar[`IMailMergeDataSource`](../), returnera namnet på data -källan från den här egenskapen.

Aspose.Words använder detta namn för att matcha mot kopplingsområdets namn specificerat i malldokumentet. Jämförelsen mellan datakällans namn och namnet på kopplingsregionens namn är inte skiftlägeskänslig.

### Exempel

Visar hur man kör en sammankoppling med en datakälla i form av ett anpassat objekt.

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

    // För att använda ett anpassat objekt som en datakälla måste det implementera IMailMergeDataSource-gränssnittet. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Ett exempel på en "data entity"-klass i din applikation.
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
/// En anpassad kopplingsdatakälla som du implementerar för att tillåta Aspose.Words 
/// för att sammanfoga data från dina kundobjekt till Microsoft Word-dokument.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // När vi initierar datakällan måste dess position vara före den första posten.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Namnet på datakällan. Används endast av Aspose.Words när e-postsammanslagning med repeterbara regioner körs.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words anropar denna metod för att få ett värde för varje datafält.
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
                // Returnera "false" till Aspose.Words kopplingsmotor för att beteckna
                // att vi inte kunde hitta ett fält med detta namn.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// En standardimplementation för att flytta till nästa post i en samling.
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

### Se även

* interface [IMailMergeDataSource](../)
* namnutrymme [Aspose.Words.MailMerging](../../imailmergedatasource/)
* hopsättning [Aspose.Words](../../../)


