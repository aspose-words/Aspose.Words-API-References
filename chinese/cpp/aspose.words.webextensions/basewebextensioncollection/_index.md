---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection 类"
linktitle: "BaseWebExtensionCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection 类。BaseWebExtensionCollection 是 TaskPaneCollection、WebExtensionBindingCollection、WebExtensionPropertyCollection 和 WebExtensionReferenceCollection 集合的基类。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.webextensions/basewebextensioncollection/
---
## BaseWebExtensionCollection class


用于 [TaskPaneCollection](../taskpanecollection/)、[WebExtensionBindingCollection](../webextensionbindingcollection/)、[WebExtensionPropertyCollection](../webextensionpropertycollection/) 和 [WebExtensionReferenceCollection](../webextensionreferencecollection/) 集合的基类。要了解更多信息，请访问 [Work with Office Add-ins](https://docs.aspose.com/words/cpp/work-with-office-add-ins/) 文档文章。

```cpp
template<typename T>class BaseWebExtensionCollection : public System::Collections::Generic::IEnumerable<T>
```


| 参数 | 描述 |
| --- | --- |
| T | 集合项的类型。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](./add/)(T) | 将指定项添加到集合中。 |
| [BaseWebExtensionCollection](./basewebextensioncollection/)() |  |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | 从集合中移除所有元素。 |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | 获取集合中包含的元素数量。 |
| [GetEnumerator](./getenumerator/)() override | 返回可遍历集合的枚举器。 |
| [idx_get](./idx_get/)(int32_t) | 获取或设置指定索引处的项。 |
| [idx_set](./idx_set/)(int32_t, T) | 获取或设置指定索引处的项。 |
| [Remove](./remove/)(int32_t) | 从集合中移除指定索引处的项。 |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| 类型定义 | 描述 |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## 示例



展示如何使用文档的 Web 扩展集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Web extension.docx");

ASSERT_EQ(1, doc->get_WebExtensionTaskPanes()->get_Count());

// 打印文档的 Web 扩展的所有属性。
System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionPropertyCollection> webExtensionPropertyCollection = doc->get_WebExtensionTaskPanes()->idx_get(0)->get_WebExtension()->get_Properties();
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty>>> enumerator = webExtensionPropertyCollection->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::WebExtensions::WebExtensionProperty> webExtensionProperty = enumerator->get_Current();
        std::cout << System::String::Format(u"Binding name: {0}; Binding value: {1}", webExtensionProperty->get_Name(), webExtensionProperty->get_Value()) << std::endl;
    }
}

// 移除 Web 扩展。
doc->get_WebExtensionTaskPanes()->Remove(0);

ASSERT_EQ(0, doc->get_WebExtensionTaskPanes()->get_Count());
```

## 另见

* Namespace [Aspose::Words::WebExtensions](../)
* Library [Aspose.Words for C++](../../)
