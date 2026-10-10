---
title: "Aspose::Words::WebExtensions::WebExtensionBindingType enum"
linktitle: "WebExtensionBindingType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WebExtensions::WebExtensionBindingType enum. Elenca i tipi disponibili di binding tra un'estensione web e i dati nel documento in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.webextensions/webextensionbindingtype/
---
## WebExtensionBindingType enum


Enumera i tipi disponibili di binding tra un'estensione web e i dati nel documento.

```cpp
enum class WebExtensionBindingType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Matrice | 0 | Dati tabulari senza riga di intestazione. |
| Table | 1 | Dati tabulari con riga di intestazione. |
| Testo | 2 | Testo semplice. |
| Default | n/a | Matrice usata per impostazione predefinita. |


## Esempi



Mostra come aggiungere un'estensione web a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un riquadro attività con l'add-in "MyScript", che sarà usato dal documento,
// poi imposta la sua posizione predefinita.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Se ci sono più riquadri attività nella stessa posizione di aggancio, possiamo impostare questo indice per organizzarli.
myScriptTaskPane->set_Row(1);

// Crea un add-in chiamato "MyScript Math Sample", che verrà visualizzato nel riquadro attività.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Imposta i parametri di riferimento dell'archivio dell'applicazione per il nostro add-in, come l'ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Consenti all'utente di interagire con l'add-in.
webExtension->set_IsFrozen(false);

// Possiamo accedere all'estensione web in Microsoft Word tramite Sviluppatore -> Componenti aggiuntivi.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Rimuovi tutti i riquadri attività dell'estensione web in una volta così.
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

## Vedi anche

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
