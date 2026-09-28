---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Указывает стиль встроенного шрифта внутри объекта FontInfo в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Указывает стиль встроенного шрифта внутри объекта [FontInfo](../fontinfo/).

```cpp
enum class EmbeddedFontStyle
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Regular | 0 | Указывает обычный встроенный шрифт. |
| Полужирный | 1 | Указывает полужирный встроенный шрифт. |
| Курсив | 2 | Указывает курсивный встроенный шрифт. |
| ПолужирныйКурсив | 3 | Указывает полужирный‑курсивный встроенный шрифт. |


## Примеры



Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальную файловую систему.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Форматы встроенных шрифтов могут отличаться в других форматах, таких как .doc.
// Нам необходимо знать правильный формат, прежде чем мы сможем извлечь шрифт.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Также мы можем преобразовать встроенный формат OpenType, полученный из документов .doc, в OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## См. также

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
