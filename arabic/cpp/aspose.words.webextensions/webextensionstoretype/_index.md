---
title: "Aspose::Words::WebExtensions::WebExtensionStoreType تعداد"
linktitle: "WebExtensionStoreType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WebExtensions::WebExtensionStoreType تعداد. يعدد الأنواع المتاحة لمتجر ملحق ويب في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.webextensions/webextensionstoretype/
---
## WebExtensionStoreType enum


يسرد الأنواع المتاحة لمتجر ملحق الويب.

```cpp
enum class WebExtensionStoreType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| SPCatalog | 0 | يحدد أن نوع المتجر هو كتالوج SharePoint المؤسسي. |
| OMEX | 1 | يحدد أن نوع المتجر هو Office.com. |
| SPApp | 2 | يحدد أن نوع المتجر هو تطبيق ويب SharePoint. |
| Exchange | 3 | يحدد أن نوع المتجر هو خادم Exchange. |
| FileSystem | 4 | يحدد أن نوع المتجر هو مشاركة نظام ملفات. |
| Registry | 5 | يحدد أن نوع المتجر هو سجل النظام. |
| ExCatalog | 6 | يحدد أن نوع المتجر هو النشر المركزي عبر Exchange. |
| افتراضي | n/a | القيمة الافتراضية. |


## أمثلة



يظهر كيفية إضافة امتداد ويب إلى مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إنشاء لوحة مهام باستخدام الإضافة "MyScript"، والتي سيستخدمها المستند،
// ثم تعيين موقعه الافتراضي.
auto myScriptTaskPane = System::MakeObject<Aspose::Words::WebExtensions::TaskPane>();
doc->get_WebExtensionTaskPanes()->Add(myScriptTaskPane);
myScriptTaskPane->set_DockState(Aspose::Words::WebExtensions::TaskPaneDockState::Right);
myScriptTaskPane->set_IsVisible(true);
myScriptTaskPane->set_Width(300);
myScriptTaskPane->set_IsLocked(true);

// إذا كانت هناك عدة لوحات مهام في نفس موقع الإرساء، يمكننا تعيين هذا الفهرس لترتيبها.
myScriptTaskPane->set_Row(1);

// إنشاء إضافة تسمى "MyScript Math Sample"، والتي ستعرضها لوحة المهام.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtension> webExtension = myScriptTaskPane->get_WebExtension();

// تعيين معلمات مرجع متجر التطبيق لإضافتنا، مثل المعرف.
webExtension->get_Reference()->set_Id(u"WA104380646");
webExtension->get_Reference()->set_Version(u"1.0.0.0");
webExtension->get_Reference()->set_StoreType(Aspose::Words::WebExtensions::WebExtensionStoreType::OMEX);
webExtension->get_Reference()->set_Store(System::Globalization::CultureInfo::get_CurrentCulture()->get_Name());
webExtension->get_Properties()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionProperty>(u"MyScript", u"MyScript Math Sample"));
webExtension->get_Bindings()->Add(System::MakeObject<Aspose::Words::WebExtensions::WebExtensionBinding>(u"MyScript", Aspose::Words::WebExtensions::WebExtensionBindingType::Text, u"104380646"));

// السماح للمستخدم بالتفاعل مع الإضافة.
webExtension->set_IsFrozen(false);

// يمكننا الوصول إلى امتداد الويب في Microsoft Word عبر المطور -> الإضافات.
doc->Save(get_ArtifactsDir() + u"Document.WebExtension.docx");

// إزالة جميع لوحات مهام امتداد الويب مرة واحدة بهذه الطريقة.
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

## انظر أيضًا

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
