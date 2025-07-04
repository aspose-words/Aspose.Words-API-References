---
title: Aspose::Words::Style::get_SemiHidden method
linktitle: get_SemiHidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_SemiHidden method. Gets/sets whether the style hides from the Styles gallery and from the Styles task pane in C++.'
type: docs
weight: 16667
url: /cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Gets/sets whether the style hides from the Styles gallery and from the Styles task pane.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
