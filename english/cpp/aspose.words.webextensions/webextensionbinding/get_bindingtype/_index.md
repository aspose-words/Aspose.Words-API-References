---
title: Aspose::Words::WebExtensions::WebExtensionBinding::get_BindingType method
linktitle: get_BindingType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WebExtensions::WebExtensionBinding::get_BindingType method. Specifies the binding type in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.webextensions/webextensionbinding/get_bindingtype/
---
## WebExtensionBinding::get_BindingType method


Specifies the binding type.

```cpp
Aspose::Words::WebExtensions::WebExtensionBindingType Aspose::Words::WebExtensions::WebExtensionBinding::get_BindingType() const
```

## Examples


Shows how to add a web extension to a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create task pane with "MyScript" add-in, which will be used by the document,
// then set its default location.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(TaskPaneDockState::Right);
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
webExtension->get_Reference()->set_StoreType(WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", WebExtensionBindingType::Text, u"104380646"));

// Allow the user to interact with the add-in.
webExtension->set_IsFrozen(false);

// We can access the web extension in Microsoft Word via Developer -> Add-ins.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Remove all web extension task panes at once like this.
doc->get_WebExtensionTaskPanes()->Clear();

ASSERT_EQ(doc->get_WebExtensionTaskPanes()->get_Count(), 0);

doc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"Document.WebExtension.docx"));

myScriptTaskPane = doc->get_WebExtensionTaskPanes()->idx_get(0);
ASSERT_EQ(myScriptTaskPane->get_DockState(), TaskPaneDockState::Right);
ASSERT_TRUE(myScriptTaskPane->get_IsVisible());
ASPOSE_ASSERT_EQ(myScriptTaskPane->get_Width(), 300.0);
ASSERT_TRUE(myScriptTaskPane->get_IsLocked());
ASSERT_EQ(myScriptTaskPane->get_Row(), 1);

webExtension = myScriptTaskPane->get_WebExtension();
ASSERT_EQ(webExtension->get_Id(), System::String::Empty);

ASSERT_EQ(webExtension->get_Reference()->get_Id(), u"WA104380646");
ASSERT_EQ(webExtension->get_Reference()->get_Version(), u"1.0.0.0");
ASSERT_EQ(webExtension->get_Reference()->get_StoreType(), WebExtensionStoreType::OMEX);
ASSERT_EQ(webExtension->get_Reference()->get_Store(), System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
ASSERT_EQ(webExtension->get_AlternateReferences()->get_Count(), 0);

ASSERT_EQ(webExtension->get_Properties()->idx_get(0)->get_Name(), u"MyScript");
ASSERT_EQ(webExtension->get_Properties()->idx_get(0)->get_Value(), u"MyScript Math Sample");

ASSERT_EQ(webExtension->get_Bindings()->idx_get(0)->get_Id(), u"MyScript");
ASSERT_EQ(webExtension->get_Bindings()->idx_get(0)->get_BindingType(), WebExtensionBindingType::Text);
ASSERT_EQ(webExtension->get_Bindings()->idx_get(0)->get_AppRef(), u"104380646");

ASSERT_FALSE(webExtension->get_IsFrozen());
```
## See Also

* Enum [WebExtensionBindingType](../../webextensionbindingtype/)
* Class [WebExtensionBinding](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
