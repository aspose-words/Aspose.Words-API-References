---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion метод"
linktitle: "get_MswVersion"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion метод. Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — Word2019 в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [Word2019](../../../aspose.words.settings/mswordversion/)

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Примеры



Показывает, как эмулировать процедуру загрузки определённой версии Microsoft Word во время загрузки документа.
```cpp
// По умолчанию Aspose.Words загружает документы в соответствии со спецификацией Microsoft Word 2019.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// В этом документе отсутствует стиль форматирования абзаца по умолчанию.
// Этот стиль по умолчанию будет восстановлен, когда мы загрузим документ либо в Microsoft Word, либо в Aspose.Words.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// Межстрочный интервал стиля будет иметь это значение при загрузке согласно спецификации Microsoft Word 2007.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## См. также

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
