---
title: "Aspose::Words::Border::get_LineStyle метод"
linktitle: "get_LineStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_LineStyle метод. Получает или задает стиль границы в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Получает или задает стиль границы.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Примечания


Если установить стиль линии в значение none, то ширина линии автоматически изменится на ноль.

## Примеры



Показывает, как вставить строку, окружённую границей, в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## См. также

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
