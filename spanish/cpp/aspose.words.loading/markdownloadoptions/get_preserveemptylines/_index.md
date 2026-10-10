---
title: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines"
linktitle: "get_PreserveEmptyLines"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines. Obtiene o establece un valor booleano que indica si se deben conservar las líneas vacías al cargar un documento Markdown. El valor predeterminado es false. Normalmente, las líneas vacías entre elementos de nivel de bloque en Markdown se ignoran. Las líneas vacías al principio y al final del documento también se ignoran. Esta opción permite importar esas líneas vacías en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Obtiene o establece un valor booleano que indica si se deben conservar las líneas vacías al cargar un documento [Markdown](../../../aspose.words/loadformat/). El valor predeterminado es **false**. Normalmente, las líneas vacías entre elementos de nivel de bloque en Markdown se ignoran. Las líneas vacías al principio y al final del documento también se ignoran. Esta opción permite importar esas líneas vacías.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
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
