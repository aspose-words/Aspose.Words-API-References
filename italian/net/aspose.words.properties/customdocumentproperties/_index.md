---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Properties.CustomDocumentProperties per gestire le proprietà personalizzate dei documenti in modo semplice. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 5190
url: /it/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Una raccolta di proprietà personalizzate del documento.

Per saperne di più, visita il[Lavorare con le proprietà del documento](https://docs.aspose.com/words/net/work-with-document-properties/) articolo di documentazione.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Ottiene il numero di elementi nella raccolta. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Restituisce un[`DocumentProperty`](../documentproperty/) oggetto per indice. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Restituisce un[`DocumentProperty`](../documentproperty/) oggetto in base al nome della proprietà. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Crea una nuova proprietà personalizzata del documentoBoolean tipo di dati. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Crea una nuova proprietà personalizzata del documentoDateTime tipo di dati. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Crea una nuova proprietà personalizzata del documentoDouble tipo di dati. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Crea una nuova proprietà personalizzata del documentoNumber tipo di dati. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Crea una nuova proprietà personalizzata del documentoString tipo di dati. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | Crea una nuova proprietà personalizzata del documento collegata al contenuto. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Rimuove tutte le proprietà dalla raccolta. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Restituisce`VERO` se nella raccolta esiste una proprietà con il nome specificato. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ottiene l'indice di una proprietà in base al nome. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Rimuove una proprietà all'indice specificato. |

## Osservazioni

Ogni[`DocumentProperty`](../documentproperty/) L'oggetto rappresenta una proprietà personalizzata di un documento contenitore.

I nomi delle proprietà non fanno distinzione tra maiuscole e minuscole.

Le proprietà nella raccolta sono ordinate alfabeticamente in base al nome.

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

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* spazio dei nomi [Aspose.Words.Properties](../../aspose.words.properties/)
* assemblea [Aspose.Words](../../)
