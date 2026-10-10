---
title: "Aspose::Words::Fonts::FontInfoCollection::Contains 方法"
linktitle: "Contains"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection::Contains 方法。确定集合是否包含具有给定名称的字体（在 C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection::Contains method


确定集合是否包含具有给定名称的字体。

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::Contains(const System::String &name)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 要定位的字体的名称（不区分大小写）。 |

### ReturnValue

**true** if the item is found in the collection; otherwise, **false**.

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
