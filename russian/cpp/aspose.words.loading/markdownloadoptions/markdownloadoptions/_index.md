---
title: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions конструктор"
linktitle: "MarkdownLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions конструктор. Инициализирует новый экземпляр класса MarkdownLoadOptions в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions::MarkdownLoadOptions constructor


Инициализирует новый экземпляр класса [MarkdownLoadOptions](../).

```cpp
Aspose::Words::Loading::MarkdownLoadOptions::MarkdownLoadOptions()
```


## Примеры



Показывает, как сохранить пустую строку при загрузке документа.
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

## См. также

* Class [MarkdownLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
