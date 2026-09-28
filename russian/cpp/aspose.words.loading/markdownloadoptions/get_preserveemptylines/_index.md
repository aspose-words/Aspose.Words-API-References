---
title: "Метод Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines"
linktitle: "get_PreserveEmptyLines"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines. Получает или задает логическое значение, указывающее, следует ли сохранять пустые строки при загрузке документа Markdown. Значение по умолчанию — false. Обычно пустые строки между блочными элементами в Markdown игнорируются. Пустые строки в начале и в конце документа также игнорируются. Эта опция позволяет импортировать такие пустые строки в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.loading/markdownloadoptions/get_preserveemptylines/
---
## MarkdownLoadOptions::get_PreserveEmptyLines method


Получает или задает логическое значение, указывающее, следует ли сохранять пустые строки при загрузке документа [Markdown](../../../aspose.words/loadformat/). Значение по умолчанию — **false**. Обычно пустые строки между блочными элементами в Markdown игнорируются. Пустые строки в начале и в конце документа также игнорируются. Эта опция позволяет импортировать такие пустые строки.

```cpp
bool Aspose::Words::Loading::MarkdownLoadOptions::get_PreserveEmptyLines() const
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
