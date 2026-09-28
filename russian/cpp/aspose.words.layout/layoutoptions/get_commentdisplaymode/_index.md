---
title: "Метод Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode"
linktitle: "get_CommentDisplayMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode. Получает или задает способ отображения комментариев. Значение по умолчанию — ShowInBalloons в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.layout/layoutoptions/get_commentdisplaymode/
---
## LayoutOptions::get_CommentDisplayMode method


Получает или задает способ отображения комментариев. Значение по умолчанию — [ShowInBalloons](../../commentdisplaymode/).

```cpp
Aspose::Words::Layout::CommentDisplayMode Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode() const
```


## Примеры



Показывает, как отображать комментарии при сохранении документа в отрисованный формат.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// ShowInAnnotations доступен только в форматах Pdf1.7 и Pdf1.5.
// В других форматах он будет работать аналогично Hide.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInAnnotations);

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInAnnotations.pdf");

// Обратите внимание, что требуется перестроить разметку страниц документа (через метод Document.UpdatePageLayout()).
// после изменения значений Document.LayoutOptions.
doc->get_LayoutOptions()->set_CommentDisplayMode(Aspose::Words::Layout::CommentDisplayMode::ShowInBalloons);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.ShowCommentsInBalloons.pdf");
```

## См. также

* Enum [CommentDisplayMode](../../commentdisplaymode/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
