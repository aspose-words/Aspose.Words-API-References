---
title: "Aspose::Words::Style::get_SemiHidden 方法"
linktitle: "get_SemiHidden"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_SemiHidden 方法。获取/设置样式是否在样式库和样式任务窗格中隐藏（C++）。"
type: docs
weight: 16667
url: /zh/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


获取/设置样式是否从“样式”画廊和“样式”任务窗格中隐藏。

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
