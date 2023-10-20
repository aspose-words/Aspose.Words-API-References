---
title: TaskPaneCollection Class
linktitle: TaskPaneCollection
articleTitle: TaskPaneCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.WebExtensions.TaskPaneCollection klas. Gibt eine Liste dauerhafter Aufgabenbereichsobjekte an in C#.
type: docs
weight: 6720
url: /de/net/aspose.words.webextensions/taskpanecollection/
---
## TaskPaneCollection class

Gibt eine Liste dauerhafter Aufgabenbereichsobjekte an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Office-Add-Ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) Dokumentationsartikel.

```csharp
public class TaskPaneCollection : BaseWebExtensionCollection<TaskPane>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } |  |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } |  |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*[TaskPane](../taskpane/)*) |  |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() |  |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() |  |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) |  |

## Beispiele

Zeigt, wie man einem Dokument eine Weberweiterung hinzufügt.

```csharp
Document doc = new Document();

// Aufgabenbereich mit „MyScript“-Add-in erstellen, der vom Dokument verwendet wird,
// dann den Standardspeicherort festlegen.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Wenn sich mehrere Aufgabenbereiche am selben Andockort befinden, können wir diesen Index festlegen, um sie anzuordnen.
myScriptTaskPane.Row = 1;

// Erstellen Sie ein Add-In mit dem Namen „MyScript Math Sample“, in dem der Aufgabenbereich angezeigt wird.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Legen Sie Referenzparameter für den Anwendungsspeicher für unser Add-In fest, z. B. die ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Dem Benutzer erlauben, mit dem Add-In zu interagieren.
webExtension.IsFrozen = false;

// Wir können über Developer -> auf die Web-Erweiterung in Microsoft Word zugreifen. Add-Ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Entfernen Sie auf diese Weise alle Aufgabenbereiche der Weberweiterung auf einmal.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* class [BaseWebExtensionCollection&lt;T&gt;](../basewebextensioncollection-1/)
* class [TaskPane](../taskpane/)
* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)
