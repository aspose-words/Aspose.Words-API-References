---
title: VariableCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words per .NET
description: Scopri se VariableCollection contiene una variabile di documento in base al nome. Semplifica la gestione dei dati e migliora l'efficienza della tua programmazione oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words/variablecollection/contains/
---
## VariableCollection.Contains method

Determina se la raccolta contiene una variabile di documento con il nome specificato.

```csharp
public bool Contains(string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| name | String | Nome della variabile del documento da individuare, senza distinzione tra maiuscole e minuscole. |

### Valore di ritorno

`VERO`se l'elemento viene trovato nella raccolta; in caso contrario,`falso`.

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

* class [VariableCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
