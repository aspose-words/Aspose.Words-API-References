---
title: Aspose::Words::Settings::ViewOptions::set_ZoomPercent method
linktitle: set_ZoomPercent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ViewOptions::set_ZoomPercent method. Sets the percentage at which you want to view your document in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.settings/viewoptions/set_zoompercent/
---
## ViewOptions::set_ZoomPercent method


Sets the percentage at which you want to view your document.

```cpp
void Aspose::Words::Settings::ViewOptions::set_ZoomPercent(int32_t value)
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

ASSERT_EQ(ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```
## See Also

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
