---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade метод"
linktitle: "get_ForeTintAndShade"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade метод. Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Получает или задает значение типа double, которое осветляет или затемняет цвет переднего плана.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Примечания


Допустимые значения находятся в диапазоне от -1 (самый темный) до 1 (самый светлый) для этого свойства.

Ноль (0) — нейтральное значение.

## Примеры



Показывает, как управлять осветлением и затемнением цвета шрифта переднего плана.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## См. также

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
