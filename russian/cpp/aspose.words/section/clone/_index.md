---
title: "Метод Aspose::Words::Section::Clone"
linktitle: "Клонировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Section::Clone. Создаёт дубликат этого раздела в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/section/clone/
---
## Section::Clone method


Создаёт дубликат этого раздела.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Section::Clone()
```


## Примеры



Показывает, как добавлять и удалять разделы в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Удалите первый раздел из документа.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Добавьте копию текущего первого раздела в конец документа.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## См. также

* Class [Section](../)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
