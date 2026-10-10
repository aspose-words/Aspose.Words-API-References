---
title: "Aspose::Words::Style::get_SemiHidden طريقة"
linktitle: "get_SemiHidden"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_SemiHidden طريقة. يحصل/يضبط ما إذا كان النمط يختفي من معرض الأنماط ومن لوحة مهام الأنماط في C++."
type: docs
weight: 16667
url: /ar/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


يحصل/يضبط ما إذا كان النمط يختفي من معرض الأنماط ومن لوحة مهام الأنماط.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
```


## أمثلة



يعرض كيفية إعطاء أولوية وإخفاء النمط.
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

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
