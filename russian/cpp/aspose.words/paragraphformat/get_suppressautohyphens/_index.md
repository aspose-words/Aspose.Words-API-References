---
title: "метод Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens"
linktitle: "get_SuppressAutoHyphens"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens метод. Указывает, следует ли освобождать текущий абзац от любой переноски, применяемой в настройках документа в C++."
type: docs
weight: 38000
url: /ru/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Указывает, следует ли исключить текущий абзац из любой переноски слов, применяемой в настройках документа.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Примеры



Показывает, как отключить переносы для абзаца.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Откройте документ, содержащий текст с локалью, соответствующей нашей словарной базе.
// При сохранении этого документа в формат фиксированных страниц его текст будет иметь переносы.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Мы можем установить свойство "SuppressAutoHyphens" в значение "true", чтобы отключить переносы
// для конкретного абзаца, оставив его включённым для остальной части документа.
// Значение свойства по умолчанию — "false",
// что означает, что каждый абзац по умолчанию использует переносы, если они доступны.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## См. также

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
