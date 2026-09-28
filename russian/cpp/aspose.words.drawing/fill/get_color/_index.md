---
title: "Метод Aspose::Words::Drawing::Fill::get_Color"
linktitle: "get_Color"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Fill::get_Color. Получает или задаёт объект Color, представляющий цвет переднего плана заливки в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.drawing/fill/get_color/
---
## Fill::get_Color method


Получает или задает объект Color, который представляет цвет переднего плана заливки.

```cpp
System::Drawing::Color Aspose::Words::Drawing::Fill::get_Color()
```


## Примеры



Показывает, как преобразовать любую из заливок обратно в сплошную заливку.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Two color gradient.docx");

// Получить объект Fill для шрифта первого Run.
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_Font()->get_Fill();

// Проверьте свойства Fill шрифта.
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill is transparent at " << (fill->get_Transparency() * 100) << "%" << std::endl;

// Измените тип заливки на Сплошную с однородным зеленым цветом.
fill->Solid();
std::cout << "\nThe fill is changed:" << std::endl;
std::cout << System::String::Format(u"The type of the fill is: {0}", fill->get_FillType()) << std::endl;
std::cout << "The foreground color of the fill is: " << fill->get_ForeColor() << std::endl;
std::cout << "The fill transparency is " << (fill->get_Transparency() * 100) << "%" << std::endl;

doc->Save(get_ArtifactsDir() + u"Drawing.FillSolid.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
