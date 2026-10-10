---
title: "Aspose::Words::Layout::CommentDisplayMode 枚举"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::CommentDisplayMode 枚举。指定 C++ 中文档注释的渲染模式。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


指定文档批注的渲染模式。

```cpp
enum class CommentDisplayMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 隐藏 | 0 | 未渲染文档批注。 |
| ShowInBalloons | 1 | 在页边的气泡中渲染文档批注。这是默认值。 |
| ShowInAnnotations | 2 | 在注释中渲染文档批注。这仅适用于 PDF 格式。 |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
