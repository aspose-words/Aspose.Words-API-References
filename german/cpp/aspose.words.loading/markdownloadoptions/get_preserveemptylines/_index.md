---
title: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines Methode"
linktitle: "get_PreserveEmptyLines"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines method. Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob leere Zeilen beim Laden eines Markdown-Dokuments erhalten bleiben sollen. Der Standardwert ist false. Normalerweise werden leere Zeilen zwischen Block‑Elementen in Markdown ignoriert. Leere Zeilen am Anfang und Ende des Dokuments werden ebenfalls ignoriert. Diese Option ermöglicht das Importieren solcher leerer Zeilen in C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Gibt einen booleschen Wert zurück oder setzt ihn, der angibt, ob leere Zeilen beim Laden eines [Markdown](../../../aspose.words/loadformat/) Dokuments erhalten bleiben sollen. Der Standardwert ist **false**. Normalerweise werden leere Zeilen zwischen Block‑Elementen in Markdown ignoriert. Leere Zeilen am Anfang und Ende des Dokuments werden ebenfalls ignoriert. Diese Option ermöglicht das Importieren solcher leerer Zeilen.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
```


## Beispiele



Zeigt, wie man eine leere Zeile beim Laden eines Dokuments beibehält.
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

## Siehe auch

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
