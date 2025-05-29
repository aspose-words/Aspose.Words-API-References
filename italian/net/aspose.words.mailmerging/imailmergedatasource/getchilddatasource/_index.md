---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words per .NET
description: Scopri come il metodo GetChildDataSource di IMailMergeDataSource migliora la stampa unione di Aspose.Words gestendo in modo fluido le regioni annidate.
type: docs
weight: 20
url: /it/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Il motore di stampa unione Aspose.Words richiama questo metodo quando incontra l'inizio di un'area di stampa unione annidata.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableName | String | Nome dell'area di stampa unione come specificato nel documento modello. Non distingue tra maiuscole e minuscole. |

### Valore di ritorno

Un oggetto sorgente dati che fornirà l'accesso ai record di dati della tabella specificata.

## Osservazioni

Quando i motori di stampa unione Aspose.Words popolano un'area di stampa unione con dati e incontrano l'inizio di un'area di stampa unione nidificata sotto forma di MERGEFIELD TableStart:TableName, richiama`GetChildDataSource` sull'oggetto sorgente dati current . L'implementazione deve restituire un nuovo oggetto sorgente dati che fornisca l'accesso ai record child del record padre corrente. Aspose.Words utilizzerà l'origine dati restituita per popolare la regione di stampa unione nidificata.

Di seguito sono riportate le regole che l'implementazione di`GetChildDataSource` deve seguire.

Se la tabella rappresentata da questo oggetto sorgente dati ha una tabella figlio correlata (dettagli) con il nome specificato, , l'implementazione deve restituire un nuovo[`IMailMergeDataSource`](../) oggetto che fornirà l'accesso ai record figlio del record corrente. Un esempio di ciò è la relazione Ordini / DettagliOrdine. Supponiamo che l'attuale[`IMailMergeDataSource`](../) object rappresenta la tabella Ordini e contiene un record di ordine corrente. Successivamente, Aspose.Words incontra "MERGEFIELD TableStart:OrderDetails" nel documento e invoca`GetChildDataSource` . Devi creare e restituire un[`IMailMergeDataSource`](../) Oggetto che consentirà ad Aspose.Words di accedere al record OrderDetails per l'ordine corrente.

Se questo oggetto di origine dati non ha una relazione con la tabella con il nome specificato, è necessario restituire a[`IMailMergeDataSource`](../)oggetto che fornirà l'accesso a tutti i record della tabella specificata.

Se una tabella con il nome specificato non esiste, l'implementazione dovrebbe restituire`null` .

## Esempi

Mostra come eseguire una stampa unione con un'origine dati sotto forma di oggetto personalizzato.

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

     // Per utilizzare un oggetto personalizzato come origine dati, è necessario implementare l'interfaccia IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Un esempio di classe "entità dati" nella tua applicazione.
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
 /// Un'origine dati di unione di posta personalizzata che puoi implementare per consentire Aspose.Words
/// per unire tramite posta i dati degli oggetti Cliente nei documenti Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Quando inizializziamo la sorgente dati, la sua posizione deve essere precedente al primo record.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Il nome dell'origine dati. Utilizzato da Aspose.Words solo quando si esegue la stampa unione con aree ripetibili.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words chiama questo metodo per ottenere un valore per ogni campo dati.
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
                // Restituisce "false" al motore di stampa unione Aspose.Words per indicare
                // che non siamo riusciti a trovare un campo con questo nome.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Un'implementazione standard per passare al record successivo in una raccolta.
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

* interface [IMailMergeDataSource](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
