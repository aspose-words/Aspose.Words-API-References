---
title: "Aspose::Words::Layout::CommentDisplayMode enum"
linktitle: "CommentDisplayMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Layout::CommentDisplayMode enum. Указывает режим отображения комментариев документа в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enum


Указывает режим отрисовки комментариев к документу.

```cpp
enum class CommentDisplayMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Hide | 0 | Комментарии документа не отображаются. |
| ShowInBalloons | 1 | Отображает комментарии документа в виде баллонов на полях. Это значение по умолчанию. |
| ShowInAnnotations | 2 | Отображает комментарии документа в аннотациях. Доступно только для формата PDF. |


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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
