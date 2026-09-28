---
title: "Метод Aspose::Words::Font::get_Position"
linktitle: "get_Position"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Position. Получает или задает позицию текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное опускает его в C++."
type: docs
weight: 32000
url: /ru/cpp/aspose.words/font/get_position/
---
## Font::get_Position method


Получает или задает позицию текста (в пунктах) относительно базовой линии. Положительное число поднимает текст, а отрицательное опускает его.

```cpp
double Aspose::Words::Font::get_Position()
```


## Примеры



Показывает, как отформатировать текст, чтобы сместить его позицию.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));

// Поднимите эту последовательность текста на 5 пунктов выше базовой линии.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Raised text. ");
run->get_Font()->set_Position(5);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Опустите эту последовательность текста на 10 пунктов ниже базовой линии.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Lowered text. ");
run->get_Font()->set_Position(-10);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Добавьте обычный фрагмент текста.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Text in its default position. ");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Добавьте фрагмент текста, отображаемый как нижний индекс.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Subscript. ");
run->get_Font()->set_Subscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Добавьте фрагмент текста, отображаемый как верхний индекс.
run = System::MakeObject<Aspose::Words::Run>(doc, u"Superscript.");
run->get_Font()->set_Superscript(true);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Font.PositionSubscript.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
