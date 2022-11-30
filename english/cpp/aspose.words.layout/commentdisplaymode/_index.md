---
title: CommentDisplayMode
second_title: Aspose.Words for C++ API Reference
description: Specifies the rendering mode for document comments.
type: docs
weight: 79
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
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = MakeObject<Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild(comment);

// ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
// In other formats, it will work similarly to Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(CommentDisplayMode::ShowInAnnotations);

doc->Save(ArtifactsDir + u"Document.ShowCommentsInAnnotations.pdf");

// Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
// after changing the Document.LayoutOptions values.
doc->get_LayoutOptions()->set_CommentDisplayMode(CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(ArtifactsDir + u"Document.ShowCommentsInBalloons.pdf");
```

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words](../../)
