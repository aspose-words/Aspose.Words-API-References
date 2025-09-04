---
title: WebExtension Class
linktitle: WebExtension
articleTitle: WebExtension
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.WebExtensions.WebExtension class, your go-to solution for creating dynamic web extensions in documents. Enhance functionality effortlessly!
type: docs
weight: 7650
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

Assert.That(doc.WebExtensionTaskPanes.Count, Is.EqualTo(0));

doc = new Document(ArtifactsDir + "Document.WebExtension.docx");

myScriptTaskPane = doc.WebExtensionTaskPanes[0];
Assert.That(myScriptTaskPane.DockState, Is.EqualTo(TaskPaneDockState.Right));
Assert.That(myScriptTaskPane.IsVisible, Is.True);
Assert.That(myScriptTaskPane.Width, Is.EqualTo(300.0d));
Assert.That(myScriptTaskPane.IsLocked, Is.True);
Assert.That(myScriptTaskPane.Row, Is.EqualTo(1));

webExtension = myScriptTaskPane.WebExtension;
Assert.That(webExtension.Id, Is.EqualTo(string.Empty));

Assert.That(webExtension.Reference.Id, Is.EqualTo("WA104380646"));
Assert.That(webExtension.Reference.Version, Is.EqualTo("1.0.0.0"));
Assert.That(webExtension.Reference.StoreType, Is.EqualTo(WebExtensionStoreType.OMEX));
Assert.That(webExtension.Reference.Store, Is.EqualTo(CultureInfo.CurrentCulture.Name));
Assert.That(webExtension.AlternateReferences.Count, Is.EqualTo(0));

Assert.That(webExtension.Properties[0].Name, Is.EqualTo("MyScript"));
Assert.That(webExtension.Properties[0].Value, Is.EqualTo("MyScript Math Sample"));

Assert.That(webExtension.Bindings[0].Id, Is.EqualTo("MyScript"));
Assert.That(webExtension.Bindings[0].BindingType, Is.EqualTo(WebExtensionBindingType.Text));
Assert.That(webExtension.Bindings[0].AppRef, Is.EqualTo("104380646"));

Assert.That(webExtension.IsFrozen, Is.False);
```

### See Also

* namespace [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* assembly [Aspose.Words](../../)
