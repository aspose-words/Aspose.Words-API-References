---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi facilmente elementi dalla tua BaseWebExtensionCollection con il nostro intuitivo metodo Remove. Semplifica la gestione dei tuoi dati oggi stesso!
type: docs
weight: 60
url: /it/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Rimuove l'elemento all'indice specificato dalla raccolta.

```csharp
public void Remove(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | Indice a base zero dell'elemento della raccolta. |

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
