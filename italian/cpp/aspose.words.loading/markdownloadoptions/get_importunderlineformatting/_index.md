---
title: "Metodo Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting. Ottiene o imposta un valore booleano che indica se riconoscere una sequenza di due caratteri più \"++\" come formattazione di testo sottolineato. Il valore predefinito è false in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


Ottiene o imposta un valore booleano che indica se riconoscere una sequenza di due caratteri più "++" come formattazione del testo sottolineato. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## Esempi



Mostra come riconoscere i caratteri più "++" come formattazione di testo sottolineato.
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

## Vedi anche

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
