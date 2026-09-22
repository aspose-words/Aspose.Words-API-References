---
title: "طريقة Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove"
linktitle: "Remove"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::WebExtensions::BaseWebExtensionCollection::Remove. يزيل العنصر عند الفهرس المحدد من المجموعة في C++."
type: docs
weight: 12000
url: /ar/cpp/aspose.words.webextensions/basewebextensioncollection/remove/
---
## BaseWebExtensionCollection::Remove method


يزيل العنصر عند الفهرس المحدد من المجموعة.

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::Remove(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | الفهرس الصفري للعنصر في المجموعة. |

## أمثلة



يوضح كيفية العمل مع مجموعة امتدادات الويب في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// اطبع جميع خصائص امتداد الويب في المستند.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// إزالة ملحق الويب.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## انظر أيضًا

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
