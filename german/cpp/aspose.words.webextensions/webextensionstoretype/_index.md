---
title: "Aspose::Words::WebExtensions::WebExtensionStoreType enum"
linktitle: "WebExtensionStoreType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WebExtensions::WebExtensionStoreType enum. Enumeriert verfügbare Typen eines Web‑Extension‑Stores in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enum


Enumeriert verfügbare Typen eines Web‑Extension‑Stores.

```cpp
enum class WebExtensionStoreType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| SPCatalog | 0 | Gibt an, dass der Store‑Typ ein SharePoint‑Firmenkatalog ist. |
| OMEX | 1 | Gibt an, dass der Store‑Typ Office.com ist. |
| SPApp | 2 | Gibt an, dass der Store‑Typ eine SharePoint‑Webanwendung ist. |
| Exchange | 3 | Gibt an, dass der Store‑Typ ein Exchange‑Server ist. |
| FileSystem | 4 | Gibt an, dass der Store‑Typ eine Dateisystemfreigabe ist. |
| Registry | 5 | Gibt an, dass der Store‑Typ die Systemregistrierung ist. |
| ExCatalog | 6 | Gibt an, dass der Store‑Typ eine zentralisierte Bereitstellung über Exchange ist. |
| Standard | n/a | Standardwert. |


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
