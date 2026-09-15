---
title: "Aspose::Words::Style::get_Priority طريقة"
linktitle: "get_Priority"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_Priority طريقة. يحصل/يضبط القيمة الصحيحة التي تمثل الأولوية لفرز الأنماط في لوحة مهام الأنماط في C++."
type: docs
weight: 16334
url: /ar/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


يحصل/يضبط القيمة الصحيحة التي تمثل الأولوية لفرز الأنماط في لوحة مهام الأنماط.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
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
