---
title: "Aspose::Words::Drawing::FillType enum"
linktitle: "FillType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::FillType enum. Указывает тип заливки для заполняемого объекта в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.drawing/filltype/
---
## FillType enum


Указывает тип заливки для заполняемого объекта.

```cpp
enum class FillType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Сплошной | 1 | Сплошная заливка. |
| Шаблонный | 2 | Шаблонная заливка. |
| Градиент | 3 | Градиентная заливка. |
| Текстурированный | 4 | Текстурированная заливка. |
| Background | 5 | [Fill](../fill/) то же, что и фон. |
| Picture | 6 | Заливка изображением. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
