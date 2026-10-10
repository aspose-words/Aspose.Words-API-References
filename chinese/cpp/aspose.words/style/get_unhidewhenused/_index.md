---
title: "Aspose::Words::Style::get_UnhideWhenUsed 方法"
linktitle: "get_UnhideWhenUsed"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_UnhideWhenUsed 方法。获取/设置当前文档中使用的样式是否从 Styles 库和 Styles 任务窗格中取消隐藏。在 C++ 中，当该使用的样式应显示在 Styles 库中时为 true。"
type: docs
weight: 19500
url: /zh/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


获取/设置当前文档中使用的样式是否从“样式”画廊和“样式”任务窗格中取消隐藏。当使用的样式应显示在“样式”画廊中时，为 True。

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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
