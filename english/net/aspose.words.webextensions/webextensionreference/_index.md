---
title: WebExtensionReference Class
linktitle: WebExtensionReference
articleTitle: WebExtensionReference
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WebExtensionReference class, your key to managing web extensions with ease. Identify providers and versions effortlessly!
type: docs
weight: 7660
url: /net/aspose.words.webextensions/webextensionreference/
---
## WebExtensionReference class

Represents the reference to a web extension. The reference is used to identify the provider location and version of the extension.

To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) documentation article.

```csharp
public class WebExtensionReference
```

## Constructors

| Name | Description |
| --- | --- |
| [WebExtensionReference](webextensionreference/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Id](../../aspose.words.webextensions/webextensionreference/id/) { get; set; } | Identifier associated with the web extension within a catalog provider. |
| [Store](../../aspose.words.webextensions/webextensionreference/store/) { get; set; } | Specifies the instance of the marketplace where the web extension is stored. |
| [StoreType](../../aspose.words.webextensions/webextensionreference/storetype/) { get; set; } | Specifies the type of marketplace. |
| [Version](../../aspose.words.webextensions/webextensionreference/version/) { get; set; } | Specifies the version of the web extension. |

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

### See Also

* namespace [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assembly [Aspose.Words](../../)
