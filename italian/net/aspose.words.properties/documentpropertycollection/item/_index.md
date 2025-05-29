---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente agli oggetti DocumentProperty con il nostro elemento DocumentPropertyCollection. Recupera le proprietà per nome per una gestione semplificata dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Restituisce un[`DocumentProperty`](../../documentproperty/) oggetto in base al nome della proprietà.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| name | Nome della proprietà da recuperare, senza distinzione tra maiuscole e minuscole. |

## Osservazioni

Resi`null` se non viene trovata una proprietà con il nome specificato.

## Esempi

Mostra come creare una proprietà di documento personalizzata che contiene una data e un'ora.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Guarda anche

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Restituisce un[`DocumentProperty`](../../documentproperty/) oggetto per indice.

```csharp
public DocumentProperty this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice a base zero del[`DocumentProperty`](../../documentproperty/) recuperare. |

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
* class [DocumentPropertyCollection](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
