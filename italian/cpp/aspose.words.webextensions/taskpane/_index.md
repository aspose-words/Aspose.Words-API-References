---
title: "Aspose::Words::WebExtensions::TaskPane classe"
linktitle: "TaskPane"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::WebExtensions::TaskPane classe. Rappresenta un oggetto task pane di un componente aggiuntivo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.webextensions/taskpane/
---
## TaskPane class


Rappresenta un oggetto task pane di un add-in. Per saperne di più, visita l'articolo di documentazione [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
class TaskPane : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_DockState](./get_dockstate/)() const | Specifica l'ultima posizione di dock di questo oggetto task pane. |
| [get_IsLocked](./get_islocked/)() const | Specifica se il task pane è bloccato al documento nell'interfaccia utente e non può essere chiuso dall'utente. |
| [get_IsVisible](./get_isvisible/)() const | Specifica se il task pane è visibile per impostazione predefinita quando il documento si apre. |
| [get_Row](./get_row/)() const | Specifica l'indice, enumerato dall'esterno verso l'interno, di questo task pane rispetto agli altri task pane persistenti ancorati nella stessa posizione predefinita. |
| [get_WebExtension](./get_webextension/)() const | Rappresenta un oggetto di estensione web. |
| [get_Width](./get_width/)() const | Specifica il valore di larghezza predefinito per questa istanza del riquadro attività. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DockState](./set_dockstate/)(Aspose::Words::WebExtensions::TaskPaneDockState) | Setter per [Aspose::Words::WebExtensions::TaskPane::get_DockState](./get_dockstate/). |
| [set_IsLocked](./set_islocked/)(bool) | Setter per [Aspose::Words::WebExtensions::TaskPane::get_IsLocked](./get_islocked/). |
| [set_IsVisible](./set_isvisible/)(bool) | Setter per [Aspose::Words::WebExtensions::TaskPane::get_IsVisible](./get_isvisible/). |
| [set_Row](./set_row/)(int32_t) | Setter per [Aspose::Words::WebExtensions::TaskPane::get_Row](./get_row/). |
| [set_Width](./set_width/)(double) | Setter per [Aspose::Words::WebExtensions::TaskPane::get_Width](./get_width/). |
| [TaskPane](./taskpane/)() |  |
| static [Type](./type/)() |  |

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
