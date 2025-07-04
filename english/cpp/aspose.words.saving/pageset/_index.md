---
title: Aspose::Words::Saving::PageSet class
linktitle: PageSet
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PageSet class. Describes a random set of pages. To learn more, visit the  documentation article in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/pageset/
---
## PageSet class


Describes a random set of pages. To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) documentation article.

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Methods

| Method | Description |
| --- | --- |
| static [get_All](./get_all/)() | Gets a set with all the pages of the document in their original order. |
| static [get_Even](./get_even/)() | Gets a set with all the even pages of the document in their original order. |
| static [get_Odd](./get_odd/)() | Gets a set with all the odd pages of the document in their original order. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Creates an one-page set based on exact page index. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Creates a page set based on exact page indices. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Creates a page set based on ranges. |
| static [Type](./type/)() |  |

## Examples



Shows how to render one page from a document to a JPEG image. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// When we save the document to the JPEG format, Aspose.Words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
