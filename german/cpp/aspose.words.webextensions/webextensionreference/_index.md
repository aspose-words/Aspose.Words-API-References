---
title: "Aspose::Words::WebExtensions::WebExtensionReference class"
linktitle: "WebExtensionReference"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WebExtensions::WebExtensionReference class. Stellt die Referenz zu einer Web-Erweiterung dar. Die Referenz wird verwendet, um den Anbieterort und die Version der Erweiterung zu identifizieren. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.webextensions/webextensionreference/
---
## WebExtensionReference class


Stellt die Referenz zu einer Web-Extension dar. Die Referenz wird verwendet, um den Standort des Anbieters und die Version der Extension zu identifizieren. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
class WebExtensionReference : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Id](./get_id/)() const | Kennung, die mit der Web-Erweiterung innerhalb eines Kataloganbieters verknüpft ist. |
| [get_Store](./get_store/)() const | Gibt die Instanz des Marktplatzes an, in dem die Web-Erweiterung gespeichert ist. |
| [get_StoreType](./get_storetype/)() const | Gibt den Typ des Marktplatzes an. |
| [get_Version](./get_version/)() const | Gibt die Version der Web-Erweiterung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Id](./set_id/)(const System::String\&) | Setter für [Aspose::Words::WebExtensions::WebExtensionReference::get_Id](./get_id/). |
| [set_Store](./set_store/)(const System::String\&) | Setter für [Aspose::Words::WebExtensions::WebExtensionReference::get_Store](./get_store/). |
| [set_StoreType](./set_storetype/)(Aspose::Words::WebExtensions::WebExtensionStoreType) | Setter für [Aspose::Words::WebExtensions::WebExtensionReference::get_StoreType](./get_storetype/). |
| [set_Version](./set_version/)(const System::String\&) | Setter für [Aspose::Words::WebExtensions::WebExtensionReference::get_Version](./get_version/). |
| static [Type](./type/)() |  |
| [WebExtensionReference](./webextensionreference/)() |  |

## Beispiele



Zeigt, wie man einem Dokument eine Web‑Extension hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle Task‑Paneel mit dem "MyScript"‑Add‑In, das vom Dokument verwendet wird,
// dann setzen Sie den Standardort fest.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Wenn es mehrere Taskbereiche am selben Andockort gibt, können wir diesen Index festlegen, um sie anzuordnen.
myScriptTaskPane->set_Row(1);

// Erstellen Sie ein Add-In mit dem Namen "MyScript Math Sample", das im Taskbereich angezeigt wird.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Legen Sie Anwendungsstore-Referenzparameter für unser Add-In fest, z. B. die ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Ermöglichen Sie dem Benutzer die Interaktion mit dem Add-In.
webExtension->set_IsFrozen(false);

// Wir können die Web-Erweiterung in Microsoft Word über Entwickler -> Add-Ins aufrufen.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Entfernen Sie alle Web-Erweiterungs-Taskbereiche auf einmal, wie folgt.
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

## Siehe auch

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
