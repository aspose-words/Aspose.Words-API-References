---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method"
linktitle: "get_IgnoreShapes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes method. 获取或设置一个布尔值，指示是否在文本中忽略形状。默认值在 C++ 中为 false。"
type: docs
weight: 11500
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreshapes/
---
## FindReplaceOptions::get_IgnoreShapes method


获取或设置一个布尔值，指示是否忽略文本中的形状。默认值为 **false**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes() const
```


## 示例



展示如何在替换文本时忽略形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Balloon, 200, 200);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

auto findReplaceOptions = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
findReplaceOptions->set_IgnoreShapes(true);
builder->get_Document()->get_Range()->Replace(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.", u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
ASSERT_EQ(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder->get_Document()->GetText().Trim());
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
