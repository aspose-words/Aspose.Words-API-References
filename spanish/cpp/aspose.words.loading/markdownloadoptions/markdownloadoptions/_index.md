---
title: "Constructor Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions"
linktitle: "MarkdownLoadOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Constructor Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions. Inicializa una nueva instancia de la clase MarkdownLoadOptions en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


Inicializa una nueva instancia de la clase [MarkdownLoadOptions](../).

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## Ejemplos



Muestra cómo preservar líneas vacías al cargar un documento.
```cpp
System::String mdText = System::String::Format(u"{0}Line1{1}{2}Line2{3}{4}", System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine(), System::Environment::get_NewLine());
{
    auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(mdText));
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::MarkdownLoadOptions>();
    loadOptions->set_PreserveEmptyLines(true);
    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    ASSERT_EQ(u"\rLine1\r\rLine2\r\f", doc->GetText());
}
```

## Ver también

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
