---
title: BaseWebExtensionCollection1.Remove
second_title: Aspose.Words per .NET API Reference
description: BaseWebExtensionCollection metodo. Rimuove dalla raccolta lelemento allindice specificato.
type: docs
weight: 60
url: /it/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Rimuove dalla raccolta l'elemento all'indice specificato.

```csharp
public void Remove(int index)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | Int32 | L'indice in base zero dell'elemento della raccolta. |

### Esempi

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

// Rimuove l'estensione web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Guarda anche

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* spazio dei nomi [Aspose.Words.WebExtensions](../../basewebextensioncollection-1/)
* assemblea [Aspose.Words](../../../)


