---
title: ViewType
second_title: Aspose.Words for C++ API Reference
description: Possible values for the view mode in Microsoft Word.
type: docs
weight: 248
url: /cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Possible values for the view mode in Microsoft Word.

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The document shall be rendered in the default view of the application. |
| Reading | 0 | The document shall be rendered in the default view of the application. |
| PageLayout | 1 | The document shall be opened in a view that displays the document as it will print. |
| Outline | 3 | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Normal | 4 | The document shall be rendered in a view optimized for outlining or creating long documents. |
| Web | 5 | The document shall be rendered in a view mimicking the way this document would be displayed in a web page. |


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

