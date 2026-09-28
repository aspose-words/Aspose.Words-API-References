---
title: "Aspose::Words::Drawing::ShadowType перечисление"
linktitle: "ShadowType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShadowType перечисление. Указывает тип тени фигуры в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words.drawing/shadowtype/
---
## ShadowType enum


Указывает тип тени фигуры.

```cpp
enum class ShadowType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| ShadowMixed | -2 | Нет предопределённых пресетов теней. |
| Shadow1 | 1 | Первый тип тени. |
| Shadow10 | 10 | Десятый тип тени. |
| Shadow11 | 11 | Одиннадцатый тип тени. |
| Shadow12 | 12 | Двенадцатый тип тени. |
| Shadow13 | 13 | Тринадцатый тип тени. |
| Shadow14 | 14 | Четырнадцатый тип тени. |
| Shadow15 | 15 | Пятнадцатый тип тени. |
| Shadow16 | 16 | Шестнадцатый тип тени. |
| Shadow17 | 17 | Семнадцатый тип тени. |
| Shadow18 | 18 | Восемнадцатый тип тени. |
| Shadow19 | 19 | Девятнадцатый тип тени. |
| Shadow2 | 2 | Второй тип тени. |
| Shadow20 | 20 | Двадцатый тип тени. |
| Shadow21 | 21 | Двадцать первый тип тени. |
| Shadow22 | 22 | Двадцать второй тип тени. |
| Shadow23 | 23 | Двадцать третий тип тени. |
| Shadow24 | 24 | Двадцать четвертый тип тени. |
| Shadow25 | 25 | Двадцать пятый тип тени. |
| Shadow26 | 26 | Двадцать шестой тип тени. |
| Shadow27 | 27 | Двадцать седьмой тип тени. |
| Shadow28 | 28 | Двадцать восьмой тип тени. |
| Shadow29 | 29 | Двадцать девятый тип тени. |
| Shadow3 | 3 | Третий тип тени. |
| Shadow30 | 30 | Тридцатый тип тени. |
| Shadow31 | 31 | Тридцать первый тип тени. |
| Shadow32 | 32 | Тридцать второй тип тени. |
| Shadow33 | 33 | Тридцать третий тип тени. |
| Shadow34 | 34 | Тридцать четвёртый тип тени. |
| Shadow35 | 35 | Тридцать пятый тип тени. |
| Shadow36 | 36 | Тридцать шестой тип тени. |
| Shadow37 | 37 | Тридцать седьмой тип тени. |
| Shadow38 | 38 | Тридцать восьмой тип тени. |
| Shadow39 | 39 | Тридцать девятый тип тени. |
| Shadow4 | 4 | Четвёртый тип тени. |
| Shadow40 | 40 | Сороковой тип тени. |
| Shadow41 | 41 | Сорок первый тип тени. |
| Shadow42 | 42 | Сорок второй тип тени. |
| Shadow43 | 43 | Сорок третий тип тени. |
| Shadow5 | 5 | Пятый тип тени. |
| Shadow6 | 6 | Шестой тип тени. |
| Shadow7 | 7 | Седьмой тип тени. |
| Shadow8 | 8 | Восьмой тип тени. |
| Shadow9 | 9 | Девятый тип тени. |


## Примеры



Показывает, как работать с форматированием тени для фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

if (shape->get_ShadowFormat()->get_Visible() && shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::Shadow2)
{
    shape->get_ShadowFormat()->set_Type(Aspose::Words::Drawing::ShadowType::Shadow7);
}

if (shape->get_ShadowFormat()->get_Type() == Aspose::Words::Drawing::ShadowType::ShadowMixed)
{
    shape->get_ShadowFormat()->Clear();
}
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
