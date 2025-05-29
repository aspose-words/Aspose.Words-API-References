---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Scopri la proprietà BaseWebExtensionCollection Item per gestire facilmente gli elementi in base all'indice. Semplifica il tuo sviluppo con una gestione efficiente dei dati oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Ottiene o imposta un elemento all'indice specificato.

```csharp
public T this[int index] { get; set; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice basato su zero dell'elemento. |

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
