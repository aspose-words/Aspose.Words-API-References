---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.WebExtensionStoreType mit verschiedenen Web-Erweiterungsspeichertypen für nahtlose Integration und erweiterte Funktionalität.
type: docs
weight: 7670
url: /de/net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Listet die verfügbaren Typen eines Web-Erweiterungsspeichers auf.

```csharp
public enum WebExtensionStoreType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| SPCatalog | `0` | Gibt an, dass der Speichertyp ein SharePoint-Unternehmenskatalog ist. |
| OMEX | `1` | Gibt an, dass der Store-Typ Office.com ist. |
| SPApp | `2` | Gibt an, dass der Store-Typ eine SharePoint-Webanwendung ist. |
| Exchange | `3` | Gibt an, dass der Speichertyp ein Exchange-Server ist. |
| FileSystem | `4` | Gibt an, dass der Speichertyp eine Dateisystemfreigabe ist. |
| Registry | `5` | Gibt an, dass der Speichertyp die Systemregistrierung ist. |
| ExCatalog | `6` | Gibt an, dass der Speichertyp „Zentralisierte Bereitstellung über Exchange“ ist. |
| Default | `0` | Standardwert. |

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
