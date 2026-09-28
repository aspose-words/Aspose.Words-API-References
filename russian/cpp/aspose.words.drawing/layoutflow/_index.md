---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::LayoutFlow enum. Определяет направление размещения текста в текстовом поле в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Определяет поток расположения текста в текстовом поле.

```cpp
enum class LayoutFlow
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Горизонтальная | 0 | Текст отображается горизонтально. |
| TopToBottomIdeographic | 1 | Идеографический текст отображается вертикально. |
| BottomToTop | 2 | Текст отображается вертикально. |
| TopToBottom | 3 | Текст отображается вертикально. |
| HorizontalIdeographic | 4 | Идеографический текст отображается горизонтально. |
| Вертикальная | 5 | Текст отображается вертикально. |


## Примеры



Показывает, как добавить текст в текстовое поле и изменить его ориентацию
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
