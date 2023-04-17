---
title: Aspose::Words::Settings::ViewOptions::get_ViewType method
linktitle: get_ViewType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ViewOptions::get_ViewType method. Controls the view mode in Microsoft Word in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.settings/viewoptions/get_viewtype/
---
## ViewOptions::get_ViewType method


Controls the view mode in Microsoft Word.

```cpp
Aspose::Words::Settings::ViewType Aspose::Words::Settings::ViewOptions::get_ViewType() const
```

## Remarks


Although Aspose.Words is able to read and write this option, its usage is application-specific. For example MS Word 2013 does not respect the value of this option.

## Examples



Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(ArtifactsDir + u"ViewOptions.SetZoomPercentage.doc");
```

## See Also

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
