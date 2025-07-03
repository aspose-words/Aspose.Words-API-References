---
title: Aspose::Words::WebExtensions::BaseWebExtensionCollection class
linktitle: BaseWebExtensionCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::WebExtensions::BaseWebExtensionCollection class. Base class for TaskPaneCollection, WebExtensionBindingCollection, WebExtensionPropertyCollection and WebExtensionReferenceCollection collections. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


Base class for [TaskPaneCollection](../taskpanecollection/), [WebExtensionBindingCollection](../webextensionbindingcollection/), [WebExtensionPropertyCollection](../webextensionpropertycollection/) and [WebExtensionReferenceCollection](../webextensionreferencecollection/) collections. To learn more, visit the [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/) documentation article.

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| Parameter | Description |
| --- | --- |
| T | Type of a collection item. |
## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(T) | Adds specified item to the collection. |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator that can iterate through a collection. |
| [idx_get](./idx_get/)(int32_t) | Gets or sets an item at the specified index. |
| [idx_set](./idx_set/)(int32_t, T) | Gets or sets an item at the specified index. |
| [Remove](./remove/)(int32_t) | Removes the item at the specified index from the collection. |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Examples



Shows how to work with a document's collection of web extensions. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// Print all properties of the document's web extension.
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// Remove the web extension.
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## See Also

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
