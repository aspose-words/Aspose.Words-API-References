---
title: BaseWebExtensionCollection1.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BaseWebExtensionCollection Count pour récupérer facilement le nombre total d'éléments, améliorant ainsi l'efficacité de votre développement Web.
type: docs
weight: 10
url: /fr/net/aspose.words.webextensions/basewebextensioncollection-1/count/
---
## BaseWebExtensionCollection&lt;T&gt;.Count property

Obtient le nombre d'éléments contenus dans la collection.

```csharp
public int Count { get; }
```

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
