---
title: "Aspose::Words::Comparing::CompareOptions::get_Granularity 方法"
linktitle: "get_Granularity"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comparing::CompareOptions::get_Granularity 方法。指定在 C++ 中更改是按字符还是按单词进行跟踪。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.comparing/compareoptions/get_granularity/
---
## CompareOptions::get_Granularity method


指定更改是按字符还是按单词进行跟踪。

```cpp
Aspose::Words::Comparing::Granularity Aspose::Words::Comparing::CompareOptions::get_Granularity() const
```


## 示例



展示在比较文档时如何指定粒度。
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>();
auto builderA = System::MakeObject<Aspose::Words::DocumentBuilder>(docA);
builderA->Writeln(u"Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

auto docB = System::MakeObject<Aspose::Words::Document>();
auto builderB = System::MakeObject<Aspose::Words::DocumentBuilder>(docB);
builderB->Writeln(u"Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// 指定是否正在跟踪更改
// 按字符（'Granularity.CharLevel'）或按单词（'Granularity.WordLevel'）。
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->set_Granularity(granularity);

docA->Compare(docB, u"author", System::DateTime::get_Now(), compareOptions);

// 第一个文档的修订组集合包含文档之间的所有差异。
System::SharedPtr<Aspose::Words::RevisionGroupCollection> groups = docA->get_Revisions()->get_Groups();
ASSERT_EQ(5, groups->get_Count());
```

## 另见

* Enum [Granularity](../../granularity/)
* Class [CompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
