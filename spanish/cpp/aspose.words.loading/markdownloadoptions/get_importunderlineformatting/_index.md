---
title: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting"
linktitle: "get_ImportUnderlineFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting. Obtiene o establece un valor booleano que indica si reconocer una secuencia de dos caracteres más \"++\" como formato de texto subrayado. El valor predeterminado es false en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.loading/markdownloadoptions/get_importunderlineformatting/
---
## MarkdownLoadOptions::get_ImportUnderlineFormatting method


Obtiene o establece un valor booleano que indica si reconocer una secuencia de dos caracteres más "++" como formato de subrayado de texto. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_ImportUnderlineFormatting() const
```


## Ejemplos



Muestra cómo reconocer los caracteres más "++" como formato de texto subrayado.
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

## Ver también

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
