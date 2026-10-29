---
title: Aspose::Words::Settings::ViewOptions class
linktitle: ViewOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::ViewOptions class. Provides various options that control how a document is shown in Microsoft Word. To learn more, visit the Work with Options and Appearance of Word Documents documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Provides various options that control how a document is shown in Microsoft Word. 
To learn more, visit the [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/) documentation article.

```cpp
class ViewOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Controls display of the background shape in print layout view. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Turns off display of the space between the top of the text and the top edge of the page. |
| [get_FormsDesign](./get_formsdesign/)() const | Specifies whether the document is in forms design mode. |
| [get_ViewType](./get_viewtype/)() const | Controls the view mode in Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Gets or sets the percentage at which you want to view your document. |
| [get_ZoomType](./get_zoomtype/)() const | Gets or sets a zoom value based on the size of the window. |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Controls display of the background shape in print layout view. |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Turns off display of the space between the top of the text and the top edge of the page. |
| [set_FormsDesign](./set_formsdesign/)(bool) | Specifies whether the document is in forms design mode. |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Controls the view mode in Microsoft Word. |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Sets the percentage at which you want to view your document. |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Sets a zoom value based on the size of the window. |
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

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
// to automatically zoom the document to fit the width of the page.
// Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
// to automatically zoom the document to make the entire first page visible.
// Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
// to automatically zoom the document to fit the inner text margins of the first page.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```
## See Also

* [Document](../../aspose.words/document/)
* [ViewOptions](../../aspose.words/document/get_viewoptions/)

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
