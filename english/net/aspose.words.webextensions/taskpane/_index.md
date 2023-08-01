---
title: TaskPane Class
linktitle: TaskPane
articleTitle: TaskPane
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.TaskPane class. Represents an addin task pane object in C#.
type: docs
weight: 6690
url: /net/aspose.words.webextensions/taskpane/
---
## TaskPane class

Represents an add-in task pane object.

To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) documentation article.

```csharp
public class TaskPane
```

## Constructors

| Name | Description |
| --- | --- |
| [TaskPane](taskpane/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DockState](../../aspose.words.webextensions/taskpane/dockstate/) { get; set; } | Specifies the last-docked location of this task pane object. |
| [IsLocked](../../aspose.words.webextensions/taskpane/islocked/) { get; set; } | Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user. |
| [IsVisible](../../aspose.words.webextensions/taskpane/isvisible/) { get; set; } | Specifies whether the task pane shows as visible by default when the document opens. |
| [Row](../../aspose.words.webextensions/taskpane/row/) { get; set; } | Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location. |
| [WebExtension](../../aspose.words.webextensions/taskpane/webextension/) { get; } | Represents an web extension object. |
| [Width](../../aspose.words.webextensions/taskpane/width/) { get; set; } | Specifies the default width value for this task pane instance. |

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
