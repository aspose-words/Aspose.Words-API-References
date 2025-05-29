---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente agli oggetti DocumentProperty con la proprietà Item BuiltInDocumentProperties. Semplifica la gestione dei tuoi documenti oggi stesso!
type: docs
weight: 140
url: /it/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Restituisce un[`DocumentProperty`](../../documentproperty/) oggetto in base al nome della proprietà.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Nome della proprietà da recuperare, senza distinzione tra maiuscole e minuscole. |

## Osservazioni

I nomi stringa delle proprietà corrispondono ai nomi delle proprietà typed disponibili da[`BuiltInDocumentProperties`](../).

Se si richiede una proprietà che non è presente nel documento, ma il nome della proprietà è riconosciuto come nome predefinito valido, viene creato un nuovo[`DocumentProperty`](../../documentproperty/) viene creato, aggiunto alla raccolta e restituito. Alla proprietà appena creata viene assegnato un valore predefinito (stringa vuota, zero,`falso` o DateTime.MinValue a seconda del tipo della proprietà incorporata).

Se si richiede una proprietà che non è presente nel documento e il nome non è riconosciuto come nome incorporato, un`null` viene restituito.

## Esempi

Mostra come lavorare con le proprietà personalizzate dei documenti.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate che, come le proprietà integrate, sono coppie chiave-valore.
 // Il documento ha un elenco fisso di proprietà predefinite. L'utente crea tutte le proprietà personalizzate.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Guarda anche

* class [DocumentProperty](../../documentproperty/)
* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
