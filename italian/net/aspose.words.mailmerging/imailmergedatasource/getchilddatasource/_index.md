---
title: GetChildDataSource
second_title: Aspose.Words per .NET API Reference
description: Il motore di stampa unione di Aspose.Words richiama questo metodo quando incontra linizio di una regione di stampa unione nidificata.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Il motore di stampa unione di Aspose.Words richiama questo metodo quando incontra l'inizio di una regione di stampa unione nidificata.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | String | Il nome dell'area della stampa unione come specificato nel documento modello. Senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

Un oggetto origine dati che fornirà l'accesso ai record di dati della tabella specificata.

### Osservazioni

Quando i motori di stampa unione di Aspose.Words popolano un'area di stampa unione con i dati e incontrano l'inizio di un'area di stampa unione annidata sotto forma di MERGEFIELD TableStart:TableName, richiama`GetChildDataSource` sull'oggetto origine dati corrente . L'implementazione deve restituire un nuovo oggetto origine dati che fornirà l'accesso ai record child del record padre corrente. Aspose.Words utilizzerà l'origine dati restituita per popolare la regione di stampa unione nidificata.

Di seguito sono riportate le regole di implementazione`GetChildDataSource` deve seguire.

Se la tabella rappresentata da questo oggetto origine dati ha una tabella figlio (dettaglio) correlata con il nome specificato, la tua implementazione deve restituire una nuova[`IMailMergeDataSource`](../../imailmergedatasource) oggetto che fornirà l'accesso ai record figlio del record corrente. Un esempio di ciò è la relazione Orders / OrderDetails. Assumiamo che la corrente[`IMailMergeDataSource`](../../imailmergedatasource) object rappresenta la tabella Ordini e ha un record dell'ordine corrente. Successivamente, Aspose.Words incontra "MERGEFIELD TableStart: OrderDetails" nel documento e invoca`GetChildDataSource` . Devi creare e restituire a[`IMailMergeDataSource`](../../imailmergedatasource) oggetto che consentirà ad Aspose.Words di accedere al record OrderDetails per l'ordine corrente.

Se questo oggetto origine dati non ha una relazione con la tabella con il nome specificato, è necessario restituire a[`IMailMergeDataSource`](../../imailmergedatasource)oggetto che fornirà l'accesso a tutti i record della tabella specificata.

Se non esiste una tabella con il nome specificato, l'implementazione dovrebbe restituire`nullo` .

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

* interface [IMailMergeDataSource](../../imailmergedatasource)
* spazio dei nomi [Aspose.Words.MailMerging](../../imailmergedatasource)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
