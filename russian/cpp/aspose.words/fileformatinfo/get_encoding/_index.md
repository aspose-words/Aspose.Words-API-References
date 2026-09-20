---
title: "Метод Aspose::Words::FileFormatInfo::get_Encoding"
linktitle: "get_Encoding"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::FileFormatInfo::get_Encoding. Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент обнаруживает кодировку только для HTML‑документов в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/fileformatinfo/get_encoding/
---
## FileFormatInfo::get_Encoding method


Получает обнаруженную кодировку, если она применима к текущему формату документа. В данный момент кодировка определяется только для HTML‑документов.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::FileFormatInfo::get_Encoding() const
```


## Примеры



Показывает, как определить кодировку в HTML‑файле.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Свойство Encoding используется только при создании объекта FileFormatInfo для html‑документа.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## См. также

* Class [FileFormatInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
