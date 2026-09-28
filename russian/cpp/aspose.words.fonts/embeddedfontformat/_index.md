---
title: "Aspose::Words::Fonts::EmbeddedFontFormat перечисление"
linktitle: "EmbeddedFontFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Указывает формат конкретного встроенного шрифта внутри объекта FontInfo. При сохранении документа в файл записываются только встроенные шрифты соответствующего формата в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Указывает формат конкретного встроенного шрифта внутри объекта [FontInfo](../fontinfo/). При сохранении документа в файл записываются только встроенные шрифты соответствующего формата.

```cpp
enum class EmbeddedFontFormat
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Указывает формат файла Embedded OpenType (EOT). Этот формат встроенных шрифтов используется в файлах DOC. |
| OpenType | 1 | Указывает шрифт, встроенный как простая копия файла шрифта OpenType (TrueType). Этот формат встроенных шрифтов используется в формате Open Office XML, включая файлы DOCX. |


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
