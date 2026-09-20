---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::GetEnumerator 方法"
linktitle: "GetEnumerator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::GetEnumerator 方法。在 C++ 中返回一个可遍历集合的枚举器。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.webextensions/basewebextensioncollection/getenumerator/
---
## BaseWebExtensionCollection::GetEnumerator method


返回可遍历集合的枚举器。

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<T>> Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::GetEnumerator() override
```


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

* Class [BaseWebExtensionCollection](../)
* Namespace [Aspose::Words::WebExtensions](../../)
* Library [Aspose.Words for C++](../../../)
