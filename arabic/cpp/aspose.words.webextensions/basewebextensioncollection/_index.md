---
title: "فئة Aspose::Words::WebExtensions::BaseWebExtensionCollection"
linktitle: "BaseWebExtensionCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::WebExtensions::BaseWebExtensionCollection. الفئة الأساسية لمجموعات TaskPaneCollection و WebExtensionBindingCollection و WebExtensionPropertyCollection و WebExtensionReferenceCollection. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


الفئة الأساسية لمجموعات [TaskPaneCollection](../taskpanecollection/)، [WebExtensionBindingCollection](../webextensionbindingcollection/)، [WebExtensionPropertyCollection](../webextensionpropertycollection/) و [WebExtensionReferenceCollection](../webextensionreferencecollection/). لمعرفة المزيد، زر مقالة الوثائق [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/).

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| معامل | الوصف |
| --- | --- |
| T | نوع عنصر في المجموعة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [Add](./add/)(T) | يضيف العنصر المحدد إلى المجموعة. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | يزيل جميع العناصر من المجموعة. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | يحصل على عدد العناصر الموجودة في المجموعة. |
| [GetEnumerator](./getenumerator/)() override | يرجع عدّادًا يمكنه التجول عبر المجموعة. |
| [idx_get](./idx_get/)(int32_t) | يحصل أو يعيّن عنصرًا عند الفهرس المحدد. |
| [idx_set](./idx_set/)(int32_t, T) | يحصل أو يعيّن عنصرًا عند الفهرس المحدد. |
| [Remove](./remove/)(int32_t) | يزيل العنصر عند الفهرس المحدد من المجموعة. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| تعريف نوع | الوصف |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
