---
title: Aspose::Words::WebExtensions::TaskPane class
linktitle: TaskPane
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WebExtensions::TaskPane class. Represents an add-in task pane object. To learn more, visit the  documentation article in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.webextensions/taskpane/
---
## TaskPane class


Represents an add-in task pane object. To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/) documentation article.

```cpp
class TaskPane : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DockState](./get_dockstate/)() const | Specifies the last-docked location of this task pane object. |
| [get_IsLocked](./get_islocked/)() const | Specifies whether the task pane is locked to the document in the UI and cannot be closed by the user. |
| [get_IsVisible](./get_isvisible/)() const | Specifies whether the task pane shows as visible by default when the document opens. |
| [get_Row](./get_row/)() const | Specifies the index, enumerating from the outside to the inside, of this task pane among other persisted task panes docked in the same default location. |
| [get_WebExtension](./get_webextension/)() const | Represents an web extension object. |
| [get_Width](./get_width/)() const | Specifies the default width value for this task pane instance. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DockState](./set_dockstate/)(Aspose::Words::WebExtensions::TaskPaneDockState) | Setter for [Aspose::Words::WebExtensions::TaskPane::get_DockState](./get_dockstate/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter for [Aspose::Words::WebExtensions::TaskPane::get_IsLocked](./get_islocked/). |
| [set_IsVisible](./set_isvisible/)(bool) | Setter for [Aspose::Words::WebExtensions::TaskPane::get_IsVisible](./get_isvisible/). |
| [set_Row](./set_row/)(int32_t) | Setter for [Aspose::Words::WebExtensions::TaskPane::get_Row](./get_row/). |
| [set_Width](./set_width/)(double) | Setter for [Aspose::Words::WebExtensions::TaskPane::get_Width](./get_width/). |
| [TaskPane](./taskpane/)() |  |
| static [Type](./type/)() |  |

## Examples



Shows how to add a web extension to a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create task pane with "MyScript" add-in, which will be used by the document,
// then set its default location.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// If there are multiple task panes in the same docking location, we can set this index to arrange them.
myScriptTaskPane->set_Row(1);

// Create an add-in called "MyScript Math Sample", which the task pane will display within.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Set application store reference parameters for our add-in, such as the ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Allow the user to interact with the add-in.
webExtension->set_IsFrozen(false);

// We can access the web extension in Microsoft Word via Developer -> Add-ins.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Remove all web extension task panes at once like this.
doc->get_WebExtensionTaskPanes()->Clear();

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.WebExtension.docx");

myScriptTaskPane = doc->get_WebExtensionTaskPanes()->idx_get(0);
ASSERT_EQ(Aspose::Words::WebExtensions::TaskPaneDockState::Right, myScriptTaskPane->get_DockState());
ASSERT_TRUE(myScriptTaskPane->get_IsVisible());
ASPOSE_ASSERT_EQ(300.0, myScriptTaskPane->get_Width());
ASSERT_TRUE(myScriptTaskPane->get_IsLocked());
ASSERT_EQ(1, myScriptTaskPane->get_Row());

webExtension = myScriptTaskPane->get_WebExtension();
ASSERT_EQ(System::String::Empty, webExtension->get_Id());

ASSERT_EQ(u"WA104380646", webExtension->get_Reference()->get_Id());
ASSERT_EQ(u"1.0.0.0", webExtension->get_Reference()->get_Version());
ASSERT_EQ(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX, webExtension->get_Reference()->get_StoreType());
ASSERT_EQ(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name(), webExtension->get_Reference()->get_Store());
ASSERT_EQ(0, webExtension->get_AlternateReferences()->get_Count());

ASSERT_EQ(u"MyScript", webExtension->get_Properties()->idx_get(0)->get_Name());
ASSERT_EQ(u"MyScript Math Sample", webExtension->get_Properties()->idx_get(0)->get_Value());

ASSERT_EQ(u"MyScript", webExtension->get_Bindings()->idx_get(0)->get_Id());
ASSERT_EQ(Aspose::Words::WebExtensions::WebExtensionBindingType::Text, webExtension->get_Bindings()->idx_get(0)->get_BindingType());
ASSERT_EQ(u"104380646", webExtension->get_Bindings()->idx_get(0)->get_AppRef());

ASSERT_FALSE(webExtension->get_IsFrozen());
```

## See Also

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
