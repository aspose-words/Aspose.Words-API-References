---
title: "Aspose::Words::WebExtensions::WebExtensionStoreType enum"
linktitle: "WebExtensionStoreType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::WebExtensions::WebExtensionStoreType enum. Enumère les types disponibles d'un magasin d'extension web en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enum


Énumère les types disponibles d'un magasin d'extension web.

```cpp
enum class WebExtensionStoreType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| SPCatalog | 0 | Spécifie que le type de magasin est le catalogue d'entreprise SharePoint. |
| OMEX | 1 | Spécifie que le type de magasin est Office.com. |
| SPApp | 2 | Spécifie que le type de magasin est une application web SharePoint. |
| Exchange | 3 | Spécifie que le type de magasin est un serveur Exchange. |
| FileSystem | 4 | Spécifie que le type de magasin est un partage de système de fichiers. |
| Registry | 5 | Spécifie que le type de magasin est le registre du système. |
| ExCatalog | 6 | Spécifie que le type de magasin est le déploiement centralisé via Exchange. |
| Default | n/a | Valeur par défaut. |


## Exemples



Montre comment ajouter une extension web à un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créer un volet de tâche avec le module complémentaire "MyScript", qui sera utilisé par le document,
// puis définir son emplacement par défaut.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// S'il y a plusieurs volets de tâche dans le même emplacement d'ancrage, nous pouvons définir cet indice pour les organiser.
myScriptTaskPane->set_Row(1);

// Créer un module complémentaire appelé "MyScript Math Sample", qui sera affiché dans le volet de tâche.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Définir les paramètres de référence du magasin d'application pour notre module complémentaire, tels que l'ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Permettre à l'utilisateur d'interagir avec le module complémentaire.
webExtension->set_IsFrozen(false);

// Nous pouvons accéder à l'extension web dans Microsoft Word via Développeur -> Modules complémentaires.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Supprimer tous les volets d'extension web d'un coup comme ceci.
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

## Voir aussi

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
