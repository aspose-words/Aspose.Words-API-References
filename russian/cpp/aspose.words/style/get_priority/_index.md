---
title: "Aspose::Words::Style::get_Priority метод"
linktitle: "get_Priority"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_Priority метод. Получает/устанавливает целочисленное значение, представляющее приоритет сортировки стилей в панели задач Styles в C++."
type: docs
weight: 16334
url: /ru/cpp/aspose.words/style/get_priority/
---
## Style::get_Priority method


Получает/устанавливает целочисленное значение, представляющее приоритет сортировки стилей в панели задач Styles.

```cpp
int32_t Aspose::Words::Style::get_Priority() const
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
