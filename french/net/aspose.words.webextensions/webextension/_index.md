---
title: WebExtension Class
linktitle: WebExtension
articleTitle: WebExtension
second_title: Aspose.Words pour .NET
description: Aspose.Words.WebExtensions.WebExtension classe. Représente un objet dextension Web en C#.
type: docs
weight: 6740
url: /fr/net/aspose.words.webextensions/webextension/
---
## WebExtension class

Représente un objet d'extension Web.

Pour en savoir plus, visitez le[Travailler avec les compléments Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) article documentaire.

```csharp
public class WebExtension
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Spécifie des références alternatives à une extension Web. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Spécifie une liste de liaisons d'extensions Web. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Identifie de manière unique l'instance d'extension Web dans le document actuel. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Spécifie si l'utilisateur peut interagir ou non avec l'extension Web. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Représente un ensemble de propriétés personnalisées d'extension Web. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Spécifie la référence principale à une extension Web. |

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

* espace de noms [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Assemblée [Aspose.Words](../../)
