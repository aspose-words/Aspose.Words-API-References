---
title: "Aspose::Words::Border::get_Shadow метод"
linktitle: "get_Shadow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Border::get_Shadow метод. Получает или задает значение, указывающее, имеет ли граница тень, в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Получает или задает значение, указывающее, имеет ли граница тень.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Примечания


В Microsoft Word, чтобы у границы была тень, границы со всех четырёх сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета, и у всех должно быть свойство Shadow, установленное в **true**.

## Примеры



Показывает, как создать зеленую волнистую границу страницы с тенью.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## См. также

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
