---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting метод"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting метод. Получает или задает логическое значение, указывающее, следует ли распознавать последовательность из двух знаков плюса \"++\" как форматирование текста подчёркиванием. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


Получает или задает логическое значение, указывающее, распознавать ли последовательность из двух знаков плюс "++" как форматирование подчёркнутого текста. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## Примеры



Показывает, как распознавать знаки плюса "++" как форматирование текста подчёркиванием.
```cpp
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_ASCII()->GetBytes(u"++12 and B++"));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    auto para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::Single, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());

    loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_ImportUnderlineFormatting(false);
    doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    para = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
    ASSERT_EQ(Aspose::Words::Underline::None, para->get_Runs()->idx_get(0)->get_Font()->get_Underline());
}
```

## См. также

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
