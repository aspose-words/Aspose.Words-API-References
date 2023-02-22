---
title: Interface IMailMergeDataSource
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.MailMerging.IMailMergeDataSource gränssnitt. Implementera detta gränssnitt för att tillåta sammanslagning av epost från en anpassad datakälla till exempel en lista med objekt. Masterdetalj data stöds också.
type: docs
weight: 3590
url: /sv/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Implementera detta gränssnitt för att tillåta sammanslagning av e-post från en anpassad datakälla, till exempel en lista med objekt. Master-detalj data stöds också.

```csharp
public interface IMailMergeDataSource
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Returnerar namnet på datakällan. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(string) | Aspose.Words kopplingsmotor anropar den här metoden när den stöter på början av en kapslad kopplingsregion. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(string, out object) | Returnerar ett värde för det angivna fältnamnet eller false om fältet inte hittas. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Avancerar till nästa post i datakällan. |

### Anmärkningar

När en datakälla skapas ska den initieras så att den pekar på BOF (före den första posten). Aspose.Words e-postsammanfogningsmotor kommer att anropa[`MoveNext`](./movenext/) för att gå vidare till nästa post och anropa sedan[`GetValue`](./getvalue/) för varje kopplingsfält som det stöter på i dokumentet eller den aktuella kopplingsregionen.

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

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)


