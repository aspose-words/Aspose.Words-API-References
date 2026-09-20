---
title: "Aspose::Words::Style::get_SemiHidden метод"
linktitle: "get_SemiHidden"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_SemiHidden метод. Получает/устанавливает, скрывается ли стиль в галерее Styles и в панели задач Styles в C++."
type: docs
weight: 16667
url: /ru/cpp/aspose.words/style/get_semihidden/
---
## Style::get_SemiHidden method


Получает/устанавливает, скрывается ли стиль в галерее Стилей и на панели задач Стилей.

```cpp
bool Aspose::Words::Style::get_SemiHidden() const
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
