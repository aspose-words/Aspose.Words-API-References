---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words pour .NET
description: BaseWebExtensionCollection Remove méthode. Supprime lélément à lindex spécifié de la collection en C#.
type: docs
weight: 60
url: /fr/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Supprime l'élément à l'index spécifié de la collection.

```csharp
public void Remove(int index)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| index | Int32 | Index de base zéro de l'élément de collection. |

## Exemples

Montre comment utiliser la collection d’extensions Web d’un document.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Imprime toutes les propriétés de l'extension Web du document.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Supprime l'extension Web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Voir également

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* espace de noms [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../../)
