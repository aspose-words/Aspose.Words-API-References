---
title: "Aspose::Words::Fonts::FontInfoCollection::get_Count 方法"
linktitle: "get_Count"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection::get_Count 方法。获取集合中包含的元素数量（在 C++ 中）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/get_count/
---
## FontInfoCollection::get_Count method


获取集合中包含的元素数量。

```cpp
int32_t Aspose::Words::Fonts::FontInfoCollection::get_Count()
```


## 示例



显示空白文档中存在的字体信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 空白文档包含 3 种默认字体。文档中的每种字体
// 将拥有相应的 FontInfo 对象，其中包含该字体的详细信息。
ASSERT_EQ(3, doc->get_FontInfos()->get_Count());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Times New Roman"));
ASSERT_EQ(204, doc->get_FontInfos()->idx_get(u"Times New Roman")->get_Charset());

ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Symbol"));
ASSERT_TRUE(doc->get_FontInfos()->Contains(u"Arial"));
```

## 另见

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
