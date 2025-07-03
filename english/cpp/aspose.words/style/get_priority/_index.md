---
title: Aspose::Words::Style::get_Priority method
linktitle: get_Priority
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_Priority method. Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane in C++.'
type: docs
weight: 16334
url: /cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
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
