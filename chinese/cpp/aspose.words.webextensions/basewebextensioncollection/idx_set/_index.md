---
title: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set 方法"
linktitle: "idx_set"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WebExtensions::BaseWebExtensionCollection::idx_set 方法。获取或设置 C++ 中指定索引处的项。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.webextensions/basewebextensioncollection/idx_set/
---
## BaseWebExtensionCollection::idx_set method


获取或设置指定索引处的项。

```cpp
void Aspose::Words::WebExtensions::BaseWebExtensionCollection<T>::idx_set(int32_t index, T value)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 项的零基索引。 |

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
