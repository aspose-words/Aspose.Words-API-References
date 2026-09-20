---
title: "Aspose::Words::Style::get_Priority 方法"
linktitle: "get_Priority"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_Priority 方法。获取/设置表示在样式任务窗格中对样式进行排序的优先级的整数值（C++）。"
type: docs
weight: 16334
url: /zh/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


获取/设置表示在“样式”任务窗格中对样式排序优先级的整数值。

```cpp
int32_t Aspose::Words::Style::get_Priority() const
```


## 示例



展示如何为样式设置优先级并隐藏它。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
