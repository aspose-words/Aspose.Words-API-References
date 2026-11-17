---
title: Aspose::Words::Style::set_UnhideWhenUsed method
linktitle: set_UnhideWhenUsed
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::set_UnhideWhenUsed method. Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words/style/set_unhidewhenused/
---
## Style::set_UnhideWhenUsed method


Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery.

```cpp
void Aspose::Words::Style::set_UnhideWhenUsed(bool value)
```

## Examples


Shows how to prioritize and hide a style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(StyleIdentifier::Subtitle);

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
## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
