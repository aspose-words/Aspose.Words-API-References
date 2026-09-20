---
title: "Aspose::Words::Border::get_LineWidth метод"
linktitle: "get_LineWidth"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_LineWidth метод. Получает или задает ширину границы в пунктах в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Получает или задает ширину границы в пунктах.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Примечания


Если установить ширину линии больше нуля, когда стиль линии равен None, стиль линии автоматически меняется на одиночную линию.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
