---
title: "Aspose::Words::WebExtensions::TaskPane class"
linktitle: "TaskPane"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WebExtensions::TaskPane class. Представляет объект панели задач надстройки. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.webextensions/taskpane/
---
## TaskPane class


Представляет объект панели задач надстройки. Чтобы узнать больше, посетите статью документации [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
class TaskPane : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DockState](./get_dockstate/)() const | Указывает последнее закреплённое положение этого объекта панели задач. |
| [get_IsLocked](./get_islocked/)() const | Указывает, закреплена ли панель задач за документом в пользовательском интерфейсе и не может ли пользователь её закрыть. |
| [get_IsVisible](./get_isvisible/)() const | Указывает, отображается ли панель задач по умолчанию при открытии документа. |
| [get_Row](./get_row/)() const | Указывает индекс, считающийся от внешнего к внутреннему, этой панели задач среди других сохранённых панелей, закреплённых в том же месте по умолчанию. |
| [get_WebExtension](./get_webextension/)() const | Представляет объект веб-расширения. |
| [get_Width](./get_width/)() const | Указывает значение ширины по умолчанию для этого экземпляра области задач. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DockState](./set_dockstate/)(Aspose::Words::WebExtensions::TaskPaneDockState) | Сеттер для [Aspose::Words::WebExtensions::TaskPane::get_DockState](./get_dockstate/). |
| [set_IsLocked](./set_islocked/)(bool) | Сеттер для [Aspose::Words::WebExtensions::TaskPane::get_IsLocked](./get_islocked/). |
| [set_IsVisible](./set_isvisible/)(bool) | Сеттер для [Aspose::Words::WebExtensions::TaskPane::get_IsVisible](./get_isvisible/). |
| [set_Row](./set_row/)(int32_t) | Сеттер для [Aspose::Words::WebExtensions::TaskPane::get_Row](./get_row/). |
| [set_Width](./set_width/)(double) | Сеттер для [Aspose::Words::WebExtensions::TaskPane::get_Width](./get_width/). |
| [TaskPane](./taskpane/)() |  |
| static [Type](./type/)() |  |

## Примеры



Shows how to add a web extension to a document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте панель задач с надстройкой "MyScript", которая будет использоваться документом,
// затем задайте её расположение по умолчанию.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Если в том же месте закрепления несколько панелей задач, мы можем задать этот индекс для их упорядочения.
myScriptTaskPane->set_Row(1);

// Создайте надстройку под названием "MyScript Math Sample", которую будет отображать панель задач.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Задайте параметры ссылки хранилища приложения для нашей надстройки, например ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Разрешите пользователю взаимодействовать с надстройкой.
webExtension->set_IsFrozen(false);

// Мы можем получить доступ к веб‑расширению в Microsoft Word через Разработчик -> Надстройки.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Удалите все панели задач веб‑расширения одновременно, как показано.
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

## См. также

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
