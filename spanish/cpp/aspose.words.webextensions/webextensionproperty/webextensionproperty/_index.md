---
title: "Aspose::Words::WebExtensions::WebExtensionProperty::WebExtensionProperty constructor"
linktitle: "WebExtensionProperty"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WebExtensions::WebExtensionProperty::WebExtensionProperty constructor. Crea una propiedad personalizada de extensión web con el nombre y valor especificados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.webextensions/webextensionproperty/webextensionproperty/
---
## WebExtensionProperty::WebExtensionProperty constructor


Crea una propiedad personalizada de extensión web con el nombre y valor especificados.

```cpp
Aspose::Words::WebExtensions::WebExtensionProperty::WebExtensionProperty(const System::String &name, const System::String &value)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | Nombre de la propiedad. |
| value | const System::String\& | Valor de la propiedad. |

## Ejemplos



Muestra cómo agregar una extensión web a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Cree un panel de tareas con el complemento "MyScript", que será utilizado por el documento,
// luego establezca su ubicación predeterminada.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Si hay varios paneles de tareas en la misma ubicación de acoplamiento, podemos establecer este índice para organizarlos.
myScriptTaskPane->set_Row(1);

// Cree un complemento llamado "MyScript Math Sample", que se mostrará dentro del panel de tareas.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Establezca los parámetros de referencia del almacén de aplicaciones para nuestro complemento, como el ID.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Permita que el usuario interactúe con el complemento.
webExtension->set_IsFrozen(false);

// Podemos acceder a la extensión web en Microsoft Word a través de Desarrollador -> Complementos.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Elimine todos los paneles de tareas de extensiones web de una vez de esta manera.
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

## Ver también

* Class [WebExtensionProperty](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
