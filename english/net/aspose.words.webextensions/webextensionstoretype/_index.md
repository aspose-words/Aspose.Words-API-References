---
title: WebExtensionStoreType Enum
linktitle: WebExtensionStoreType
articleTitle: WebExtensionStoreType
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.WebExtensionStoreType enum. Enumerates available types of a web extension store in C#.
type: docs
weight: 7020
url: /net/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enumeration

Enumerates available types of a web extension store.

```csharp
public enum WebExtensionStoreType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| SPCatalog | `0` | Specifies that the store type is SharePoint corporate catalog. |
| OMEX | `1` | Specifies that the store type is Office.com. |
| SPApp | `2` | Specifies that the store type is a SharePoint web application. |
| Exchange | `3` | Specifies that the store type is an Exchange server. |
| FileSystem | `4` | Specifies that the store type is a file system share. |
| Registry | `5` | Specifies that the store type is the system registry. |
| ExCatalog | `6` | Specifies that the store type is Centralized Deployment via Exchange. |
| Default | `0` | Default value. |

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
