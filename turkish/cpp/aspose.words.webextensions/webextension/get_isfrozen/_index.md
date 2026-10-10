---
title: "Aspose::Words::WebExtensions::WebExtension::get_IsFrozen yöntemi"
linktitle: "get_IsFrozen"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WebExtensions::WebExtension::get_IsFrozen yöntemi. C++'da kullanıcının web uzantısıyla etkileşime girip giremeyeceğini belirtir."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.webextensions/webextension/get_isfrozen/
---
## WebExtension::get_IsFrozen method


Kullanıcının web uzantısıyla etkileşime girip giremeyeceğini belirtir.

```cpp
bool Aspose::Words::WebExtensions::WebExtension::get_IsFrozen() const
```


## Örnekler



Bir belgeye web uzantısı eklemenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Belge tarafından kullanılacak "MyScript" eklentisi ile görev bölmesi oluşturun,
// daha sonra varsayılan konumunu ayarlayın.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// Aynı yerleştirme konumunda birden fazla görev bölmesi varsa, bunları düzenlemek için bu indeksi ayarlayabiliriz.
myScriptTaskPane->set_Row(1);

// Görev bölmesinin içinde görüntüleneceği "MyScript Math Sample" adlı bir eklenti oluşturun.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// Eklentimiz için uygulama mağazası referans parametrelerini, örneğin kimliği, ayarlayın.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// Kullanıcının eklentiyle etkileşime girmesine izin ver.
webExtension->set_IsFrozen(false);

// Microsoft Word'de web uzantısına Geliştirici -> Eklentiler üzerinden erişebiliriz.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// Tüm web uzantısı görev bölmelerini bir kerede bu şekilde kaldırın.
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

## Ayrıca Bakınız

* Class [WebExtension](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
