---
title: WebExtension
second_title: Aspose.Words for C++ API Reference
description: Represents a web extension object.
type: docs
weight: 40
url: /cpp/aspose.words.webextensions/webextension/
---
## WebExtension class


Represents a web extension object.

```cpp
class WebExtension : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_AlternateReferences](./get_alternatereferences/)() const | Specifies alternate references to a web extension. |
| [get_Bindings](./get_bindings/)() const | Specifies a list of web extension bindings. |
| [get_Id](./get_id/)() const | Uniquely identifies the web extension instance in the current document. |
| [get_IsFrozen](./get_isfrozen/)() const | Specifies whether the user can interact with the web extension or not. |
| [get_Properties](./get_properties/)() const | Represents a set of web extension custom properties. |
| [get_Reference](./get_reference/)() const | Specifies the primary reference to an web extension. |
| [set_Id](./set_id/)(const System::String\&) | Uniquely identifies the web extension instance in the current document. |
| [set_IsFrozen](./set_isfrozen/)(bool) | Setter for [Aspose::Words::WebExtensions::WebExtension::get_IsFrozen](./get_isfrozen/). |

## Examples



Shows how to add a web extension to a document. 
```cpp
auto doc = MakeObject<Document>();

// Create task pane with "MyScript" add-in, which will be used by the document,
// then set its default location.
auto myScriptTaskPane = MakeObject<TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// If there are multiple task panes in the same docking location, we can set this index to arrange them.
myScriptTaskPane->set_Row(1);

// Create an add-in called "MyScript Math Sample", which the task pane will display within.
SharedPtr<WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Set application store reference parameters for our add-in, such as the ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(MakeObject<WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(MakeObject<WebExtensionBinding>(u"MyScript", WebExtensionBindingType::Text, u"104380646"));

// Allow the user to interact with the add-in.
webExtension->set_IsFrozen(false);

// We can access the web extension in Microsoft Word via Developer -> Add-ins.
doc->Save(ArtifactsDir + u"Document.WebExtension.docx");

// Remove all web extension task panes at once like this.
doc->get_WebExtensionTaskPanes()->Clear();

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## See Also

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words](../../)
