---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.VariableCollection, gestisci e personalizza in modo efficiente le variabili dei documenti per una maggiore automazione e flessibilità dei documenti.
type: docs
weight: 7380
url: /it/net/aspose.words/variablecollection/
---
## VariableCollection class

Una raccolta di variabili del documento.

Per saperne di più, visita il[Lavorare con le proprietà del documento](https://docs.aspose.com/words/net/work-with-document-properties/) articolo di documentazione.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Ottiene o imposta una variabile di documento in base al nome senza distinzione tra maiuscole e minuscole. `null` valori non sono consentiti come lato destro dell'assegnazione e saranno sostituiti da una stringa vuota. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | Aggiunge una variabile di documento alla raccolta. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | Determina se la raccolta contiene una variabile di documento con il nome specificato. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutte le variabili nella raccolta. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | Restituisce l'indice basato su zero della variabile del documento specificata nella raccolta. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | Rimuove una variabile di documento con il nome specificato dalla raccolta. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | Rimuove una variabile del documento all'indice specificato. |

## Osservazioni

I nomi e i valori delle variabili sono stringhe.

I nomi delle variabili non fanno distinzione tra maiuscole e minuscole.

## Esempi

Mostra come lavorare con la raccolta di variabili di un documento.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Ogni documento ha una raccolta di variabili di coppia chiave/valore, a cui possiamo aggiungere elementi.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Possiamo visualizzare i valori delle variabili nel corpo del documento utilizzando i campi DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// L'assegnazione di valori alle chiavi esistenti le aggiornerà.
variables.Add("Home address", "456 Queen St.");

// Dovremo quindi aggiornare i campi DOCVARIABLE per garantire che visualizzino un valore aggiornato.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Verifica che esistano variabili del documento con un certo nome o valore.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// La raccolta di variabili ordina automaticamente le variabili in ordine alfabetico in base al nome.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Enumera la raccolta di variabili.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Di seguito sono riportati tre metodi per rimuovere le variabili del documento da una raccolta.
// 1 - Per nome:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Per indice:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Cancella l'intera collezione in una volta sola:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
