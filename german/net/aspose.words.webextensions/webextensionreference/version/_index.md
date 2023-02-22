---
title: WebExtensionReference.Version
second_title: Aspose.Words für .NET-API-Referenz
description: WebExtensionReference eigendom. Gibt die Version der Weberweiterung an.
type: docs
weight: 50
url: /de/net/aspose.words.webextensions/webextensionreference/version/
---
## WebExtensionReference.Version property

Gibt die Version der Weberweiterung an.

```csharp
public string Version { get; set; }
```

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

* class [WebExtensionReference](../)
* namensraum [Aspose.Words.WebExtensions](../../webextensionreference/)
* Montage [Aspose.Words](../../../)


