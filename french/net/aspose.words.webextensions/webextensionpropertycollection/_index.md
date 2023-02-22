---
title: Class WebExtensionPropertyCollection
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.WebExtensions.WebExtensionPropertyCollection classe. Spécifie un ensemble de propriétés personnalisées dextension Web.
type: docs
weight: 6480
url: /fr/net/aspose.words.webextensions/webextensionpropertycollection/
---
## WebExtensionPropertyCollection class

Spécifie un ensemble de propriétés personnalisées d'extension Web.

```csharp
public class WebExtensionPropertyCollection : BaseWebExtensionCollection<WebExtensionProperty>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(WebExtensionProperty) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) |  |

### Exemples

Montre comment ajouter une extension Web à un document.

```csharp
Document doc = new Document();

// Créer un volet des tâches avec le complément "MyScript", qui sera utilisé par le document,
// puis définit son emplacement par défaut.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// S'il y a plusieurs volets de tâches dans le même emplacement d'ancrage, nous pouvons définir cet index pour les organiser.
myScriptTaskPane.Row = 1;

// Créez un complément appelé "MyScript Math Sample", dans lequel le volet des tâches s'affichera.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Définir les paramètres de référence du magasin d'applications pour notre complément, tels que l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Autoriser l'utilisateur à interagir avec le complément.
webExtension.IsFrozen = false;

// Nous pouvons accéder à l'extension Web dans Microsoft Word via Developer -> Compléments.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Supprimer tous les volets de tâches d'extension Web à la fois comme ceci.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Voir également

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [WebExtensionProperty](../webextensionproperty/)
* espace de noms [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../)


