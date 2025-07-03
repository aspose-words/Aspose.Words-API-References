---
title: Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode method
linktitle: get_CommentDisplayMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode method. Gets or sets the way comments are rendered. Default value is ShowInBalloons in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


Gets or sets the way comments are rendered. Default value is [ShowInBalloons](../../commentdisplaymode/).

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## Examples



Shows how to show comments when saving a document to a rendered format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
// In other formats, it will work similarly to Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
// after changing the Document.LayoutOptions values.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## See Also

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
