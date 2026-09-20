---
title: "Aspose::Words::Section::PrependContent метод"
linktitle: "PrependContent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Section::PrependContent метод. Вставляет копию содержимого исходного раздела в начало этого раздела в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/section/prependcontent/
---
## Section::PrependContent method


Вставляет копию содержимого исходного раздела в начало этого раздела.

```cpp
void Aspose::Words::Section::PrependContent(const System::SharedPtr<Aspose::Words::Section> &sourceSection)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceSection | const System::SharedPtr\<Aspose::Words::Section\>\& | Раздел, из которого копировать содержимое. |
## Примечания


Копируется только содержимое [Body](../get_body/) исходного раздела, настройки страницы, колонтитулы не копируются.

Узлы автоматически импортируются, если исходный раздел принадлежит другому документу.

Новый раздел в целевом документе не создаётся.

## Примеры



Показывает, как добавить содержимое одного раздела к другому разделу.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

System::SharedPtr<Aspose::Words::Section> section = doc->get_Sections()->idx_get(2);

ASSERT_EQ(System::String(u"Section 3") + Aspose::Words::ControlChar::SectionBreak(), section->GetText());

// Вставьте содержимое первого раздела в начало третьего раздела.
System::SharedPtr<Aspose::Words::Section> sectionToPrepend = doc->get_Sections()->idx_get(0);
section->PrependContent(sectionToPrepend);

// Вставьте содержимое второго раздела в конец третьего раздела.
System::SharedPtr<Aspose::Words::Section> sectionToAppend = doc->get_Sections()->idx_get(1);
section->AppendContent(sectionToAppend);

// Методы "PrependContent" и "AppendContent" не создали новых разделов.
ASSERT_EQ(3, doc->get_Sections()->get_Count());
ASSERT_EQ(System::String(u"Section 1") + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 3" + Aspose::Words::ControlChar::ParagraphBreak() + u"Section 2" + Aspose::Words::ControlChar::SectionBreak(), section->GetText());
```

## См. также

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
