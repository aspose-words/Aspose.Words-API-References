---
title: WebExtension.Bindings
linktitle: Bindings
articleTitle: Bindings
second_title: Aspose.Words pour .NET
description: WebExtension Bindings propriété. Spécifie une liste de liaisons dextensions Web en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.webextensions/webextension/bindings/
---
## WebExtension.Bindings property

Spécifie une liste de liaisons d'extensions Web.

```csharp
public WebExtensionBindingCollection Bindings { get; }
```

## Exemples

Montre comment ajouter une extension Web à un document.

```csharp
Document doc = new Document();

// Créer un volet de tâches avec le complément "MyScript", qui sera utilisé par le document,
// puis définit son emplacement par défaut.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// S'il existe plusieurs volets de tâches dans le même emplacement d'accueil, nous pouvons définir cet index pour les organiser.
myScriptTaskPane.Row = 1;

// Créez un complément appelé "MyScript Math Sample", dans lequel le volet des tâches affichera.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Définissez les paramètres de référence du magasin d'applications pour notre complément, tels que l'ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Autorise l'utilisateur à interagir avec le complément.
webExtension.IsFrozen = false;

// Nous pouvons accéder à l'extension Web dans Microsoft Word via Developer -> Compléments.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Supprimez tous les volets de tâches de l'extension Web en même temps, comme ceci.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Voir également

* class [WebExtensionBindingCollection](../../webextensionbindingcollection/)
* class [WebExtension](../)
* espace de noms [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../../)
