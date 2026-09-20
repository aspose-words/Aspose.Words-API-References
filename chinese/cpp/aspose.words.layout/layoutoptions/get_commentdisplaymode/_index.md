---
title: "Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode 方法"
linktitle: "get_CommentDisplayMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode 方法。获取或设置评论的呈现方式。默认值在 C++ 中为 ShowInBalloons。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


获取或设置评论的呈现方式。默认值为 [ShowInBalloons](../../commentdisplaymode/)。

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## 示例



展示在将文档保存为渲染格式时如何显示批注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations 仅在 Pdf1.7 和 Pdf1.5 格式中可用。
// 在其他格式中，它的工作方式类似于 Hide。
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// 请注意，需要重新构建文档页面布局（通过 Document.UpdatePageLayout() 方法）
// 在更改 Document.LayoutOptions 值之后。
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## 另见

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
