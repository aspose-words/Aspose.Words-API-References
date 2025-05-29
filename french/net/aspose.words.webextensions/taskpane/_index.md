---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.WebExtensions.TaskPane, votre clé pour créer de puissants volets de tâches complémentaires pour une édition de documents et une productivité améliorées.
type: docs
weight: 7560
url: /fr/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Représente un objet de volet des tâches de complément.

Pour en savoir plus, visitez le[Travailler avec les compléments Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) article de documentation.

```csharp
public class TaskPane
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Spécifie le dernier emplacement ancré de cet objet du volet Office. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Spécifie si le volet Office est verrouillé sur le document dans l'interface utilisateur et ne peut pas être fermé par l'utilisateur. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Spécifie si le volet Office s'affiche comme visible par défaut lorsque le document s'ouvre. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Spécifie l'index, énumérant de l'extérieur vers l'intérieur, de ce volet de tâches parmi d'autres volets de tâches persistants ancrés dans le même emplacement par défaut. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Représente un objet d'extension Web. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Spécifie la valeur de largeur par défaut pour cette instance du volet Office. |

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
