---
title: Class TaskPane
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.WebExtensions.TaskPane klas. Stellt ein AddInAufgabenbereichsobjekt dar.
type: docs
weight: 6710
url: /de/net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Stellt ein Add-In-Aufgabenbereichsobjekt dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Office-Add-Ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) Dokumentationsartikel.

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
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Gibt den zuletzt angedockten Speicherort dieses Aufgabenbereichsobjekts an. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Gibt an, ob der Aufgabenbereich für das Dokument in der Benutzeroberfläche gesperrt ist und vom Benutzer nicht geschlossen werden kann. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Gibt an, ob der Aufgabenbereich beim Öffnen des Dokuments standardmäßig sichtbar angezeigt wird. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Gibt den von außen nach innen aufgezählten Index dieses Aufgabenbereichs neben anderen persistenten Aufgabenbereichen an, die am selben Standardspeicherort angedockt sind. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Stellt ein Weberweiterungsobjekt dar. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Gibt den Standardbreitenwert für diese Aufgabenbereichsinstanz an. |

### Beispiele

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

* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)


