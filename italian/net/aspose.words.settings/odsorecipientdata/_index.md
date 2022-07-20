---
title: OdsoRecipientData
second_title: Aspose.Words per .NET API Reference
description: Rappresenta le informazioni su un singolo record allinterno di unorigine dati esterna che deve essere esclusa dalla stampa unione.
type: docs
weight: 5630
url: /it/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

Rappresenta le informazioni su un singolo record all'interno di un'origine dati esterna che deve essere esclusa dalla stampa unione.

```csharp
public class OdsoRecipientData
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active) { get; set; } | Specifica se il record dall'origine dati deve essere importato in un documento quando viene eseguita la stampa unione. Il valore predefinito è`VERO` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column) { get; set; } | Specifica la colonna all'interno dell'origine dati che contiene dati univoci per il record corrente. Il valore predefinito è 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash) { get; set; } | Rappresenta il codice hash per questo record. A volte utilizza Microsoft Word[`Hash`](./hash) di un intero record invece di a[`UniqueTag`](./uniquetag) valore. Il valore predefinito è 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag) { get; set; } | Specifica il contenuto di un determinato record nella colonna contenente dati univoci. Il valore predefinito è`nullo` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone)() | Restituisce un clone profondo di questo oggetto. |

### Osservazioni

Se un record deve essere unito in un documento unito, non sono necessarie informazioni su quel record. Tuttavia, se un determinato record non deve essere unito in un documento unito, il valore della chiave univoca per quel record deve essere memorizzato nel[`UniqueTag`](./uniquetag) proprietà di questo oggetto per indicare tale esclusione.

### Esempi

Mostra come accedere alla raccolta di dati che designa quali record di origine dati unire verranno esclusi da un'unione di posta.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// Possiamo clonare gli elementi in questa raccolta.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// Possiamo anche rimuovere elementi singolarmente o cancellare l'intera raccolta in una volta.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->