---
title: WebExtensionProperty
linktitle: WebExtensionProperty
articleTitle: WebExtensionProperty
second_title: Aspose.Words für .NET
description: WebExtensionProperty constructeur. Erstellt eine benutzerdefinierte Weberweiterungseigenschaft mit dem angegebenen Namen und Wert in C#.
type: docs
weight: 10
url: /de/net/aspose.words.webextensions/webextensionproperty/webextensionproperty/
---
## WebExtensionProperty constructor

Erstellt eine benutzerdefinierte Weberweiterungseigenschaft mit dem angegebenen Namen und Wert.

```csharp
public WebExtensionProperty(string name, string value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Name des Anwesens. |
| value | String | Eigentumswert. |

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

* class [WebExtensionProperty](../)
* namensraum [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../../)
