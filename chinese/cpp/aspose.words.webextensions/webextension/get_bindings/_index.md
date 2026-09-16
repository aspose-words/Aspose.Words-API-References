---
title: "Aspose::Words::WebExtensions::WebExtension::get_Bindings 方法"
linktitle: "get_Bindings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WebExtensions::WebExtension::get_Bindings 方法。指定在 C++ 中的 Web 扩展绑定列表。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.webextensions/webextension/get_bindings/
---
## WebExtension::get_Bindings method


指定 Web 扩展绑定的列表。

```cpp
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionBindingCollection> Aspose::Words::WebExtensions::WebExtension::get_Bindings() const
```


## 示例



展示如何向文档添加 Web 扩展。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建带有 "MyScript" 加载项的任务窗格，该加载项将被文档使用，
// 然后设置其默认位置。
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// 如果同一停靠位置有多个任务窗格，我们可以设置此索引来排列它们。
myScriptTaskPane->set_Row(1);

// 创建名为 "MyScript Math Sample" 的加载项，任务窗格将在其中显示。
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// 为我们的加载项设置应用商店引用参数，例如 ID。
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// 允许用户与加载项交互。
webExtension->set_IsFrozen(false);

// 我们可以通过 Developer -> Add-ins 在 Microsoft Word 中访问 Web 扩展。
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// 这样一次性移除所有 Web 扩展任务窗格。
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

## 另见

* Class [WebExtensionBindingCollection](../../webextensionbindingcollection/)
* Class [WebExtension](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
