---
title: Aspose::Words::Style::get_UnhideWhenUsed method
linktitle: get_UnhideWhenUsed
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_UnhideWhenUsed method. Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery in C++.'
type: docs
weight: 19500
url: /cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane. True when the used style should be shown in the Styles gallery.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
```


## Examples



Shows how to prioritize and hide a style. 
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

## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
