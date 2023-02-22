---
title: Interface IMailMergeDataSource
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.MailMerging.IMailMergeDataSource interfaccia. Implementa questa interfaccia per consentire la stampa unione da unorigine dati personalizzata come un elenco di oggetti. Sono supportati anche i dati di dettaglio principale.
type: docs
weight: 3590
url: /it/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Implementa questa interfaccia per consentire la stampa unione da un'origine dati personalizzata, come un elenco di oggetti. Sono supportati anche i dati di dettaglio principale.

```csharp
public interface IMailMergeDataSource
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Restituisce il nome dell'origine dati. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(string) | Il motore di stampa unione di Aspose.Words richiama questo metodo quando incontra l'inizio di una regione di stampa unione nidificata. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(string, out object) | Restituisce un valore per il nome del campo specificato o false se il campo non viene trovato. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Avanza al record successivo nell'origine dati. |

### Osservazioni

Quando viene creata un'origine dati, dovrebbe essere inizializzata in modo che punti a BOF (prima del primo record). Il motore di stampa unione di Aspose.Words invocherà[`MoveNext`](./movenext/) per passare al record successivo e quindi richiamare[`GetValue`](./getvalue/) per ogni campo di unione che incontra nel documento o nell'area di stampa unione corrente.

### Esempi

Mostra come eseguire una stampa unione con un'origine dati sotto forma di un oggetto personalizzato.

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

    // Per utilizzare un oggetto personalizzato come origine dati, è necessario implementare l'interfaccia IMailMergeDataSource. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Un esempio di una classe "entità dati" nell'applicazione.
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
/// Un'origine dati di stampa unione personalizzata che implementi per consentire Aspose.Words 
/// per inviare i dati dalla stampa unione dagli oggetti Cliente ai documenti di Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Quando si inizializza l'origine dati, la sua posizione deve essere prima del primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo durante l'esecuzione della stampa unione con aree ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo di dati.
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
                // Restituisce "false" al motore di stampa unione di Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Un'implementazione standard per passare a un record successivo in una raccolta.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)


