---
title: WebExtensionReference Class
linktitle: WebExtensionReference
articleTitle: WebExtensionReference
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.WebExtensionReference, la clé pour gérer facilement les extensions Web. Identifiez facilement les fournisseurs et les versions !
type: docs
weight: 7650
url: /fr/net/aspose.words.webextensions/webextensionreference/
---
## WebExtensionReference class

représente la référence à une extension web. Cette référence permet d'identifier l'emplacement et la version du fournisseur de l'extension.

Pour en savoir plus, visitez le[Travailler avec les compléments Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) article de documentation.

```csharp
public class WebExtensionReference
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [WebExtensionReference](webextensionreference/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [Id](../../aspose.words.webextensions/webextensionreference/id/) { get; set; } | Identifiant associé à l'extension Web au sein d'un fournisseur de catalogue. |
| [Store](../../aspose.words.webextensions/webextensionreference/store/) { get; set; } | Spécifie l'instance du marché où l'extension Web est stockée. |
| [StoreType](../../aspose.words.webextensions/webextensionreference/storetype/) { get; set; } | Spécifie le type de marché. |
| [Version](../../aspose.words.webextensions/webextensionreference/version/) { get; set; } | Spécifie la version de l'extension Web. |

## Exemples

Montre comment ajouter une extension Web à un document.

```csharp
Document doc = new Document();

// Créer un volet des tâches avec le complément « MyScript », qui sera utilisé par le document,
// puis définissez son emplacement par défaut.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// S'il existe plusieurs volets de tâches dans le même emplacement d'ancrage, nous pouvons définir cet index pour les organiser.
myScriptTaskPane.Row = 1;

// Créez un complément appelé « MyScript Math Sample », dans lequel le volet des tâches s'affichera.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Définissez les paramètres de référence de l'App Store pour notre complément, tels que l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Autoriser l'utilisateur à interagir avec le complément.
webExtension.IsFrozen = false;

// Nous pouvons accéder à l'extension Web dans Microsoft Word via Développeur -> Modules complémentaires.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Supprimez tous les volets de tâches d'extension Web à la fois comme ceci.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);

doc = new Document(ArtifactsDir + "Document.WebExtension.docx");

myScriptTaskPane = doc.WebExtensionTaskPanes[0];
Assert.AreEqual(TaskPaneDockState.Right, myScriptTaskPane.DockState);
Assert.True(myScriptTaskPane.IsVisible);
Assert.AreEqual(300.0d, myScriptTaskPane.Width);
Assert.True(myScriptTaskPane.IsLocked);
Assert.AreEqual(1, myScriptTaskPane.Row);

webExtension = myScriptTaskPane.WebExtension;
Assert.AreEqual(string.Empty, webExtension.Id);

Assert.AreEqual("WA104380646", webExtension.Reference.Id);
Assert.AreEqual("1.0.0.0", webExtension.Reference.Version);
Assert.AreEqual(WebExtensionStoreType.OMEX, webExtension.Reference.StoreType);
Assert.AreEqual(CultureInfo.CurrentCulture.Name, webExtension.Reference.Store);
Assert.AreEqual(0, webExtension.AlternateReferences.Count);

Assert.AreEqual("MyScript", webExtension.Properties[0].Name);
Assert.AreEqual("MyScript Math Sample", webExtension.Properties[0].Value);

Assert.AreEqual("MyScript", webExtension.Bindings[0].Id);
Assert.AreEqual(WebExtensionBindingType.Text, webExtension.Bindings[0].BindingType);
Assert.AreEqual("104380646", webExtension.Bindings[0].AppRef);

Assert.False(webExtension.IsFrozen);
```

### Voir également

* espace de noms [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../)
