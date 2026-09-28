---
title: "Метод Aspose::Words::Font::get_TintAndShade"
linktitle: "get_TintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_TintAndShade. Получает или задает двойное значение, которое осветляет или затемняет цвет, в C++."
type: docs
weight: 54000
url: /ru/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Получает или задаёт двойное значение, которое осветляет или затемняет цвет.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый темный) до 1 (самый светлый) для этого свойства.

Ноль (0) — нейтральное значение.

## Примеры



Показывает, как создавать и использовать стили темы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Создайте стиль с параметрами шрифтов темы.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
