---
title: "Aspose::Words::WebExtensions::TaskPaneDockState enum"
linktitle: "TaskPaneDockState"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::WebExtensions::TaskPaneDockState enum. Enumererar tillgängliga platser för uppgiftsfönsterobjekt i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.webextensions/taskpanedockstate/
---
## TaskPaneDockState enum


Enumererar tillgängliga platser för uppgiftsfönsterobjektet.

```cpp
enum class TaskPaneDockState
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Höger | 0 | Docka uppgiftsfönstret på högra sidan av dokumentfönstret. |
| Vänster | 1 | Docka uppgiftsfönstret på vänstra sidan av dokumentfönstret. |


## Exempel



Visar hur man lägger till en web extension i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa en uppgiftspanel med \"MyScript\"-tillägget, som kommer att användas av dokumentet,
// sätt sedan dess standardplats.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Om det finns flera uppgiftspaneler på samma dockningsplats kan vi ange detta index för att ordna dem.
myScriptTaskPane->set_Row(1);

// Skapa ett tillägg kallat \"MyScript Math Sample\", som uppgiftspanelen kommer att visa.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Ställ in applikationsbutiksreferensparametrar för vårt tillägg, såsom ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Tillåt användaren att interagera med tillägget.
webExtension->set_IsFrozen(false);

// Vi kan komma åt web extension i Microsoft Word via Utvecklare -> Tillägg.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Ta bort alla web extension-uppgiftspaneler på en gång så här.
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

## Se även

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
