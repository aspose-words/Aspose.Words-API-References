---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Item de BaseWebExtensionCollection pour gérer facilement les éléments par index. Simplifiez votre développement grâce à une gestion efficace des données dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

Obtient ou définit un élément à l'index spécifié.

```csharp
public T this[int index] { get; set; }
```

| Paramètre | La description |
| --- | --- |
| index | Index de base zéro de l'élément. |

## Exemples

Montre comment travailler avec la collection d'extensions Web d'un document.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Imprimez toutes les propriétés de l'extension Web du document.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Supprimez l'extension Web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Voir également

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* espace de noms [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../../)
