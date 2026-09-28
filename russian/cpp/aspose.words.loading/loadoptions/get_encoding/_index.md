---
title: "метод Aspose::Words::Loading::LoadOptions::get_Encoding"
linktitle: "get_Encoding"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Loading::LoadOptions::get_Encoding. Получает или задает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM документа, если кодировка не указана в документе. Может быть null. По умолчанию null в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Получает или задает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть **null**. По умолчанию **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Примечания


Это свойство используется только при загрузке HTML, TXT или CHM документов.

Если кодировка не указана в документе и это свойство имеет значение **null**, система попытается автоматически определить кодировку.

## Примеры



Показывает, как задать кодировку для открытия документа.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Загрузите документ, передав объект LoadOptions, затем проверьте содержимое документа.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
