---
title: Aspose::Words::Document::get_ViewOptions method
linktitle: get_ViewOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_ViewOptions method. Provides options to control how the document is displayed in Microsoft Word in C++.'
type: docs
weight: 58000
url: /cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Provides options to control how the document is displayed in Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


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


Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
// to automatically zoom the document to fit the width of the page.
// Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
// to automatically zoom the document to make the entire first page visible.
// Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
// to automatically zoom the document to fit the inner text margins of the first page.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(ArtifactsDir + u"ViewOptions.SetZoomType.doc");
```

## See Also

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
