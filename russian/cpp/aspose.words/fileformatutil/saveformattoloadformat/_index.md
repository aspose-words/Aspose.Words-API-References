---
title: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat метод"
linktitle: "SaveFormatToLoadFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat метод. Преобразует значение SaveFormat в значение LoadFormat, если это возможно, в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil::SaveFormatToLoadFormat method


Преобразует значение [SaveFormat](../../saveformat/) в значение [LoadFormat](../../loadformat/), если это возможно.

```cpp
static Aspose::Words::LoadFormat Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat saveFormat)
```


## Примеры



Показывает, как преобразовать формат сохранения в соответствующий формат загрузки.
```cpp
ASSERT_EQ(Aspose::Words::LoadFormat::Html, Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Html));

// Некоторые типы файлов могут поддерживать сохранение документов, но не загрузку с использованием Aspose.Words.
// Если попытаться преобразовать формат сохранения такого типа в формат загрузки, будет выброшено исключение.
ASSERT_THROW(static_cast<std::function<void()>>([]() -> void
{
    Aspose::Words::FileFormatUtil::SaveFormatToLoadFormat(Aspose::Words::SaveFormat::Jpeg);
})(), System::ArgumentException);
```

## См. также

* Enum [LoadFormat](../../loadformat/)
* Enum [SaveFormat](../../saveformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
