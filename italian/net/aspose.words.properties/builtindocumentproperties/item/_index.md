---
title: BuiltInDocumentProperties.Item
second_title: Aspose.Words per .NET API Reference
description: BuiltInDocumentProperties proprietà. Restituisce aDocumentProperty oggetto dal nome della proprietà.
type: docs
weight: 130
url: /it/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Restituisce a[`DocumentProperty`](../../documentproperty/) oggetto dal nome della proprietà.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Il nome senza distinzione tra maiuscole e minuscole della proprietà da recuperare. |

### Osservazioni

I nomi di stringa delle proprietà corrispondono ai nomi delle proprietà typed disponibili da[`BuiltInDocumentProperties`](../).

Se richiedi una proprietà che non è presente nel documento, ma il nome della proprietà è riconosciuto come un nome predefinito valido, un nuovo[`DocumentProperty`](../../documentproperty/) viene creato, aggiunto alla raccolta e restituito. Alla proprietà appena creata viene assegnato un valore predefinito (stringa vuota, zero, false o DateTime.MinValue a seconda del tipo della proprietà incorporata).

Se richiedi una proprietà che non è presente nel documento e il nome non viene riconosciuto come nome predefinito, viene restituito un valore null.

### Esempi

Mostra come lavorare con le proprietà del documento personalizzate.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Ogni documento contiene una raccolta di proprietà personalizzate che, come le proprietà integrate, sono coppie chiave-valore.
// Il documento ha un elenco fisso di proprietà integrate. L'utente crea tutte le proprietà personalizzate. 
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
* spazio dei nomi [Aspose.Words.Properties](../../builtindocumentproperties/)
* assemblea [Aspose.Words](../../../)


