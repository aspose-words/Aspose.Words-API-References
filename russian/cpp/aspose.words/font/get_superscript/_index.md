---
title: "Aspose::Words::Font::get_Superscript метод"
linktitle: "get_Superscript"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Superscript. Истина, если шрифт отформатирован как надстрочный в C++."
type: docs
weight: 46000
url: /ru/cpp/aspose.words/font/get_superscript/
---
## Font::get_Superscript method


Истина, если шрифт отформатирован как верхний индекс.

```cpp
bool Aspose::Words::Font::get_Superscript()
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
