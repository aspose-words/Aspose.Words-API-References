---
title: WebExtension Class
linktitle: WebExtension
articleTitle: WebExtension
second_title: Aspose.Words for .NET
description: Aspose.Words.WebExtensions.WebExtension class. Represents a web extension object in C#.
type: docs
weight: 6910
url: /net/aspose.words.webextensions/webextension/
---
## WebExtension class

Represents a web extension object.

To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) documentation article.

```csharp
public class WebExtension
```

## Properties

| Name | Description |
| --- | --- |
| [AlternateReferences](../../aspose.words.webextensions/webextension/alternatereferences/) { get; } | Specifies alternate references to a web extension. |
| [Bindings](../../aspose.words.webextensions/webextension/bindings/) { get; } | Specifies a list of web extension bindings. |
| [Id](../../aspose.words.webextensions/webextension/id/) { get; set; } | Uniquely identifies the web extension instance in the current document. |
| [IsFrozen](../../aspose.words.webextensions/webextension/isfrozen/) { get; set; } | Specifies whether the user can interact with the web extension or not. |
| [Properties](../../aspose.words.webextensions/webextension/properties/) { get; } | Represents a set of web extension custom properties. |
| [Reference](../../aspose.words.webextensions/webextension/reference/) { get; } | Specifies the primary reference to an web extension. |

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
