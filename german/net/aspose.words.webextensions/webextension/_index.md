---
title: Class WebExtension
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.WebExtensions.WebExtension klas. Stellt ein Weberweiterungsobjekt dar.
type: docs
weight: 6430
url: /de/net/aspose.words.webextensions/webextension/
---
## WebExtension class

Stellt ein Weberweiterungsobjekt dar.

```csharp
public class WebExtension
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Gibt alternative Verweise auf eine Weberweiterung an. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Gibt eine Liste von Weberweiterungsbindungen an. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Identifiziert die Weberweiterungsinstanz im aktuellen Dokument eindeutig. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Gibt an, ob der Benutzer mit der Weberweiterung interagieren kann oder nicht. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Stellt eine Reihe von benutzerdefinierten Eigenschaften für Weberweiterungen dar. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Gibt den primären Verweis auf eine Weberweiterung an. |

### Beispiele

Zeigt, wie Sie einem Dokument eine Weberweiterung hinzufügen.

```csharp
Document doc = new Document();

// Aufgabenbereich mit "MyScript"-Add-In erstellen, das vom Dokument verwendet wird,
// dann den Standardspeicherort festlegen.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// Wenn sich mehrere Aufgabenbereiche am selben Andockort befinden, können wir diesen Index festlegen, um sie anzuordnen.
myScriptTaskPane.Row = 1;

// Erstellen Sie ein Add-In namens "MyScript Math Sample", in dem der Aufgabenbereich angezeigt wird.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Anwendungsspeicher-Referenzparameter für unser Add-In festlegen, z. B. die ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Dem Benutzer erlauben, mit dem Add-In zu interagieren.
webExtension.IsFrozen = false;

// Wir können auf die Weberweiterung in Microsoft Word über Entwickler zugreifen -> Add-Ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// So entfernen Sie alle Aufgabenbereiche der Weberweiterung auf einmal.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)


