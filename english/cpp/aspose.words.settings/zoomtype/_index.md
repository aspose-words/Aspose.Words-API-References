---
title: Aspose::Words::Settings::ZoomType enum
linktitle: ZoomType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ZoomType enum. Possible values for how large or small the document appears on the screen in Microsoft Word in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Possible values for how large or small the document appears on the screen in Microsoft Word.

```cpp
enum class ZoomType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Custom | 0 | Zoom percentage is set explicitly. It is not recalculated automatically when control size changes. |
| None | n/a | Indicates to use the explicit zoom percentage. Same as [Custom](./). |
| FullPage | 1 | Zoom percentage is automatically recalculated to fit one full page. |
| PageWidth | 2 | Zoom percentage is automatically recalculated to fit page width. |
| TextFit | 3 | Zoom percentage is automatically recalculated to fit text. |


## Examples



Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
