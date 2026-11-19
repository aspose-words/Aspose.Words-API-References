---
title: Aspose::Words::Settings::ViewOptions::set_ViewType method
linktitle: set_ViewType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ViewOptions::set_ViewType method. Controls the view mode in Microsoft Word in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.settings/viewoptions/set_viewtype/
---
## ViewOptions::set_ViewType method


Controls the view mode in Microsoft Word.

```cpp
void Aspose::Words::Settings::ViewOptions::set_ViewType(Aspose::Words::Settings::ViewType value)
```

## Remarks


Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.
## Examples


Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(doc->get_ViewOptions()->get_ZoomType(), ZoomType::Custom);
ASSERT_EQ(doc->get_ViewOptions()->get_ZoomType(), ZoomType::None);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```
## See Also

* [get_ViewType](../get_viewtype/)

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
