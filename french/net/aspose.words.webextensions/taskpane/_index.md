---
title: Class TaskPane
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.WebExtensions.TaskPane classe. Représente un objet du volet des tâches du complément.
type: docs
weight: 6710
url: /fr/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Représente un objet du volet des tâches du complément.

Pour en savoir plus, visitez le[Travailler avec les compléments Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) article documentaire.

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
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Spécifie le dernier emplacement ancré de cet objet du volet des tâches. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Spécifie si le volet des tâches est verrouillé sur le document dans l'interface utilisateur et ne peut pas être fermé par l'utilisateur. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Spécifie si le volet des tâches s'affiche comme visible par défaut à l'ouverture du document. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Spécifie l'index, énumérant de l'extérieur vers l'intérieur, de ce volet de tâches parmi d'autres volets de tâches persisted ancrés au même emplacement par défaut. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Représente un objet d'extension Web. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Spécifie la valeur de largeur par défaut pour cette instance du volet Office. |

### Exemples

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


