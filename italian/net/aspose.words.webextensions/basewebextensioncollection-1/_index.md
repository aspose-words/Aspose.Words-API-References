---
title: BaseWebExtensionCollectionT Class
linktitle: BaseWebExtensionCollectionT
articleTitle: BaseWebExtensionCollectionT
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.WebExtensions.BaseWebExtensionCollection1T, il tuo strumento essenziale per gestire in modo efficiente le raccolte TaskPane e WebExtension.
type: docs
weight: 7550
url: /it/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Classe base per[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) E[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) collezioni.

Per saperne di più, visita il[Lavorare con i componenti aggiuntivi di Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) articolo di documentazione.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parametro | Descrizione |
| --- | --- |
| T | Tipo di elemento di una collezione. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Ottiene o imposta un elemento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*T*) | Aggiunge l'elemento specificato alla raccolta. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Restituisce un enumeratore che può scorrere una raccolta. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) | Rimuove l'elemento all'indice specificato dalla raccolta. |

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

* spazio dei nomi [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assemblea [Aspose.Words](../../)
