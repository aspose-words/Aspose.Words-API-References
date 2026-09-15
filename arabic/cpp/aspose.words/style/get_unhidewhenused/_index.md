---
title: "Aspose::Words::Style::get_UnhideWhenUsed طريقة"
linktitle: "get_UnhideWhenUsed"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Style::get_UnhideWhenUsed طريقة. يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه من معرض الأنماط ومن لوحة مهام الأنماط. True عندما يجب إظهار النمط المستخدم في معرض الأنماط في C++."
type: docs
weight: 19500
url: /ar/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه مرة أخرى في معرض الأنماط ومن لوحة مهام الأنماط. يكون صحيحًا عندما يجب إظهار النمط المستخدم في معرض الأنماط.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
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
