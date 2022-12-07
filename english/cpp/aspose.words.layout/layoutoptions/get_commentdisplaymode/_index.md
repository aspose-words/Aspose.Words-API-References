---
title: get_CommentDisplayMode
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the way comments are rendered. Default value is ShowInBalloons.
type: docs
weight: 40
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

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words](../../../)
