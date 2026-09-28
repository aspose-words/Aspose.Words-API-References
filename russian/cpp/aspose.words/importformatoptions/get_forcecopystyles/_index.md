---
title: "Метод Aspose::Words::ImportFormatOptions::get_ForceCopyStyles"
linktitle: "get_ForceCopyStyles"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_ForceCopyStyles. Получает или задает логическое значение, указывающее, следует ли копировать конфликтующие стили в режиме KeepSourceFormatting. Значение по умолчанию — false в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Получает или задает логическое значение, указывающее, следует ли копировать конфликтующие стили в режиме [KeepSourceFormatting](../../importformatmode/). Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Примечания


По умолчанию, если в целевом документе уже существует соответствующий стиль, форматирование исходного стиля разворачивается в прямые атрибуты узла, а стиль этого узла сбрасывается к значению по умолчанию.

Когда эта опция установлена в **true**, исходный стиль будет принудительно скопирован в целевой документ с уникальным именем и применён к импортированному узлу.

Обратите внимание, в этом случае нет гарантии, что форматирование импортированного узла в целевом документе будет сохранено.

## Примеры



Показывает, как принудительно копировать исходные стили с уникальными именами.
```cpp
// Оба документа содержат MyStyle1 и MyStyle2, MyStyle3 существует только в исходном документе.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
