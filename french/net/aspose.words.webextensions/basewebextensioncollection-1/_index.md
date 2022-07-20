---
title: BaseWebExtensionCollectionT
second_title: Référence de l'API Aspose.Words pour .NET
description: Classe de base pourTaskPaneCollection./taskpanecollection WebExtensionBindingCollection./webextensionbindingcollection  WebExtensionPropertyCollection./webextensionpropertycollection etWebExtensionReferenceCollection./webextensionreferencecollection collections.
type: docs
weight: 6390
url: /fr/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Classe de base pour[`TaskPaneCollection`](../taskpanecollection) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection) et[`WebExtensionReferenceCollection`](../webextensionreferencecollection) collections.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Paramètre | La description |
| --- | --- |
| T | Type d'élément de collection. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection`1/count) { get; } | Obtient le nombre d'éléments contenus dans la collection. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection`1/item) { get; set; } | Obtient ou définit un élément à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection`1/add)(T) | Ajoute l'élément spécifié à la collection. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection`1/clear)() | Supprime tous les éléments de la collection. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection`1/getenumerator)() | Renvoie un énumérateur qui peut parcourir une collection. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection`1/remove)(int) | Supprime l'élément à l'index spécifié de la collection. |

### Exemples

Montre comment utiliser la collection d'extensions Web d'un document.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Affiche toutes les propriétés de l'extension Web du document.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Supprimer l'extension Web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Voir également

* espace de noms [Aspose.Words.WebExtensions](../../aspose.words.webextensions)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->