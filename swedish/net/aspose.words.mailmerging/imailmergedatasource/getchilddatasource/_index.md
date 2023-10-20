---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words för .NET
description: IMailMergeDataSource GetChildDataSource metod. Aspose.Words kopplingsmotor anropar den här metoden när den stöter på början av en kapslad kopplingsregion i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Aspose.Words kopplingsmotor anropar den här metoden när den stöter på början av en kapslad kopplingsregion.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableName | String | Namnet på kopplingsområdet enligt malldokumentet. Fallet okänslig. |

### Returvärde

Ett datakällaobjekt som ger åtkomst till dataposterna i den angivna tabellen.

## Anmärkningar

När Aspose.Words kopplingsmotorer fyller en kopplingsregion med data och stöter på början av en nästlad kopplingsregion i form av MERGEFIELD TableStart:TableName, anropar den`GetChildDataSource` på datakällobjektet current . Din implementering måste returnera ett nytt datakällobjekt som ger åtkomst till child -posterna för den aktuella överordnade posten. Aspose.Words kommer att använda den returnerade datakällan för att fylla i den kapslade kopplingsregionen.

Nedan följer reglerna som genomförandet av`GetChildDataSource` måste följa.

Om tabellen som representeras av detta datakällobjekt har en relaterad underordnad (detalj) tabell med det angivna namnet, måste din implementering returnera en ny[`IMailMergeDataSource`](../)objekt som ger access till underordnade poster för den aktuella posten. Ett exempel på detta är Order/OrderDetails-relationen. Låt oss anta att strömmen[`IMailMergeDataSource`](../) object representerar tabellen Order och den har en aktuell orderpost. Därefter stöter Aspose.Words på "MERGEFIELD TableStart:OrderDetails" i dokumentet och anropar`GetChildDataSource` . Du måste skapa och returnera en[`IMailMergeDataSource`](../) objekt som tillåter Aspose.Words att komma åt OrderDetails-posten för den aktuella ordern.

Om detta datakällobjekt inte har en relation till tabellen med det angivna namnet måste du returnera a[`IMailMergeDataSource`](../) objekt som ger åtkomst till alla poster i den angivna tabellen.

Om en tabell med det angivna namnet inte finns, bör din implementering returneras`null` .

## Exempel

Visar hur man kör en sammankoppling med en datakälla i form av ett anpassat objekt.

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
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
