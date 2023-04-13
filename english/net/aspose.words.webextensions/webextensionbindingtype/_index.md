---
title: WebExtensionBindingType Enum
linktitle: WebExtensionBindingType
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.WebExtensions.WebExtensionBindingType enum. Enumerates available types of binding between a web extension and the data in the document in C#.
type: docs
weight: 6580
url: /net/aspose.words.webextensions/webextensionbindingtype/
---
## WebExtensionBindingType enumeration

Enumerates available types of binding between a web extension and the data in the document.

```csharp
public enum WebExtensionBindingType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Matrix | `0` | Tabular data without a header row. |
| Table | `1` | Tabular data with a header row. |
| Text | `2` | Plain text. |
| Default | `0` |  |

## Examples

Shows how to add a web extension to a document.

```csharp
Document doc = new Document();

// Create task pane with "MyScript" add-in, which will be used by the document,
// then set its default location.
TaskPane myScriptTaskPane = new TaskPane();
doc.WebExtensionTaskPanes.Add(myScriptTaskPane);
myScriptTaskPane.DockState = TaskPaneDockState.Right;
myScriptTaskPane.IsVisible = true;
myScriptTaskPane.Width = 300;
myScriptTaskPane.IsLocked = true;

// If there are multiple task panes in the same docking location, we can set this index to arrange them.
myScriptTaskPane.Row = 1;

// Create an add-in called "MyScript Math Sample", which the task pane will display within.
WebExtension webExtension = myScriptTaskPane.WebExtension;

// Set application store reference parameters for our add-in, such as the ID.
webExtension.Reference.Id = "WA104380646";
webExtension.Reference.Version = "1.0.0.0";
webExtension.Reference.StoreType = WebExtensionStoreType.OMEX;
webExtension.Reference.Store = CultureInfo.CurrentCulture.Name;
webExtension.Properties.Add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
webExtension.Bindings.Add(new WebExtensionBinding("MyScript", WebExtensionBindingType.Text, "104380646"));

// Allow the user to interact with the add-in.
webExtension.IsFrozen = false;

// We can access the web extension in Microsoft Word via Developer -> Add-ins.
doc.Save(ArtifactsDir + "Document.WebExtension.docx");

// Remove all web extension task panes at once like this.
doc.WebExtensionTaskPanes.Clear();

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### See Also

* namespace [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assembly [Aspose.Words](../../)
