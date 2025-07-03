---
title: Aspose::Words::Layout::CommentDisplayMode enum
linktitle: CommentDisplayMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::CommentDisplayMode enum. Specifies the rendering mode for document comments in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Specifies the rendering mode for document comments.

```cpp
enum class CommentDisplayMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Hide | 0 | No document comments are rendered. |
| ShowInBalloons | 1 | Renders document comments in balloons in the margin. This is the default value. |
| ShowInAnnotations | 2 | Renders document comments in annotations. This is only available for Pdf format. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
