---
title: BaseWebExtensionCollection1.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà BaseWebExtensionCollection Count per recuperare facilmente il numero totale di elementi, migliorando l'efficienza dello sviluppo web.
type: docs
weight: 10
url: /it/net/aspose.words.webextensions/basewebextensioncollection-1/count/
---
## BaseWebExtensionCollection&lt;T&gt;.Count property

Ottiene il numero di elementi contenuti nella raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come lavorare con la raccolta di estensioni web di un documento.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Stampa tutte le proprietà dell'estensione web del documento.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Rimuovere l'estensione web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Guarda anche

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* spazio dei nomi [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* assemblea [Aspose.Words](../../../)
