---
title: "Aspose::Words::WebExtensions::TaskPane class"
linktitle: "TaskPane"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WebExtensions::TaskPane class. 表示一个加载项任务窗格对象。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.webextensions/taskpane/
---
## TaskPane class


表示一个加载项任务窗格对象。了解更多，请访问 [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/) 文档文章。

```cpp
class TaskPane : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DockState](./get_dockstate/)() const | 指定此任务窗格对象的最后停靠位置。 |
| [get_IsLocked](./get_islocked/)() const | 指定任务窗格在 UI 中是否锁定到文档且用户无法关闭。 |
| [get_IsVisible](./get_isvisible/)() const | 指定文档打开时任务窗格是否默认可见。 |
| [get_Row](./get_row/)() const | 指定此任务窗格在同一默认位置停靠的其他持久任务窗格中的索引（从外到内枚举）。 |
| [get_WebExtension](./get_webextension/)() const | 表示一个 web extension 对象。 |
| [get_Width](./get_width/)() const | 指定此任务窗格实例的默认宽度值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DockState](./set_dockstate/)(Aspose::Words::WebExtensions::TaskPaneDockState) | 用于设置 [Aspose::Words::WebExtensions::TaskPane::get_DockState](./get_dockstate/)。 |
| [set_IsLocked](./set_islocked/)(bool) | 用于设置 [Aspose::Words::WebExtensions::TaskPane::get_IsLocked](./get_islocked/)。 |
| [set_IsVisible](./set_isvisible/)(bool) | 用于设置 [Aspose::Words::WebExtensions::TaskPane::get_IsVisible](./get_isvisible/)。 |
| [set_Row](./set_row/)(int32_t) | 用于设置 [Aspose::Words::WebExtensions::TaskPane::get_Row](./get_row/)。 |
| [set_Width](./set_width/)(double) | 用于设置 [Aspose::Words::WebExtensions::TaskPane::get_Width](./get_width/)。 |
| [TaskPane](./taskpane/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
