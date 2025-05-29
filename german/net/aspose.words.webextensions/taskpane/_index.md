---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.WebExtensions.TaskPane, Ihren Schlüssel zum Erstellen leistungsstarker Add-In-Aufgabenbereiche für verbesserte Dokumentbearbeitung und Produktivität.
type: docs
weight: 7560
url: /de/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Stellt ein Add-In-Aufgabenbereichsobjekt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Office-Add-Ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) Dokumentationsartikel.

```csharp
public class TaskPane
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [TaskPane](taskpane/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Gibt die letzte angedockte Position dieses Aufgabenbereichobjekts an. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Gibt an, ob der Aufgabenbereich in der Benutzeroberfläche an das Dokument gebunden ist und vom Benutzer nicht geschlossen werden kann. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Gibt an, ob der Aufgabenbereich beim Öffnen des Dokuments standardmäßig sichtbar ist. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Gibt den Index dieses Aufgabenbereichs unter anderen persistenten Aufgabenbereichen an, die am gleichen Standardspeicherort angedockt sind (von außen nach innen aufgezählt). |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Stellt ein Web-Erweiterungsobjekt dar. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Gibt den Standardbreitenwert für diese Aufgabenbereichsinstanz an. |

## Beispiele

Zeigt, wie einem Dokument eine Weberweiterung hinzugefügt wird.

```csharp
Document doc = new Document();

// Aufgabenbereich mit dem Add-In „MyScript“ erstellen, der vom Dokument verwendet wird,
// und legen Sie dann den Standardspeicherort fest.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Wenn sich mehrere Aufgabenbereiche am selben Andockort befinden, können wir diesen Index festlegen, um sie anzuordnen.
myScriptTaskPane.Row = 1;

// Erstellen Sie ein Add-In namens „MyScript Math Sample“, das im Aufgabenbereich angezeigt wird.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Legen Sie Anwendungsspeicher-Referenzparameter für unser Add-In fest, beispielsweise die ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Erlaubt dem Benutzer die Interaktion mit dem Add-In.
webExtension.IsFrozen = false;

// Wir können auf die Weberweiterung in Microsoft Word über Entwickler -> Add-Ins zugreifen.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Entfernen Sie auf diese Weise alle Aufgabenbereiche der Weberweiterung auf einmal.
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

### Siehe auch

* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)
