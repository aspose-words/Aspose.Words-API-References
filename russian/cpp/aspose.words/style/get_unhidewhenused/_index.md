---
title: "Метод Aspose::Words::Style::get_UnhideWhenUsed"
linktitle: "get_UnhideWhenUsed"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Style::get_UnhideWhenUsed. Получает/устанавливает, скрывается ли стиль, используемый в текущем документе, из галереи стилей и панели задач стилей. True, когда используемый стиль должен отображаться в галерее стилей в C++."
type: docs
weight: 19500
url: /ru/cpp/aspose.words/style/get_unhidewhenused/
---
## Style::get_UnhideWhenUsed method


Получает/устанавливает, отображается ли используемый в текущем документе стиль в галерее Стилей и на панели задач Стилей. Истина, когда используемый стиль должен отображаться в галерее Стилей.

```cpp
bool Aspose::Words::Style::get_UnhideWhenUsed() const
```


## Примеры



Показывает, как задать приоритет и скрыть стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Style> styleTitle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Subtitle);

if (styleTitle->get_Priority() == 9)
{
    styleTitle->set_Priority(10);
}

if (!styleTitle->get_UnhideWhenUsed())
{
    styleTitle->set_UnhideWhenUsed(true);
}

if (styleTitle->get_SemiHidden())
{
    styleTitle->set_SemiHidden(true);
}

doc->Save(get_ArtifactsDir() + u"Styles.StylePriority.docx");
```

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
