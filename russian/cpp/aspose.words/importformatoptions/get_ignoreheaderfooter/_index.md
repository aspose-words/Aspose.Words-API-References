---
title: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter метод"
linktitle: "get_IgnoreHeaderFooter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter метод. Получает или задает логическое значение, которое указывает, что форматирование содержимого заголовков/нижних колонтитулов источника игнорируется, если используется режим KeepSourceFormatting. Значение по умолчанию — true в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/importformatoptions/get_ignoreheaderfooter/
---
## ImportFormatOptions::get_IgnoreHeaderFooter method


Получает или задает логическое значение, которое указывает, что форматирование содержимого заголовков/нижних колонтитулов источника игнорируется, если используется режим [KeepSourceFormatting](../../importformatmode/). Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_IgnoreHeaderFooter() const
```


## Примеры



Показывает, как указать игнорирование или сохранение форматирования содержимого заголовков/нижних колонтитулов источника.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Если 'IgnoreHeaderFooter' равно false, то оригинальное форматирование содержимого заголовка/нижнего колонтитула
// будет использован файл "Header and footer types.docx".
// Если 'IgnoreHeaderFooter' равно true, то форматирование содержимого заголовка/нижнего колонтитула
// будет использован файл "Document.docx".
auto importFormatOptions = System::MakeObject<Aspose::Words::ImportFormatOptions>();
importFormatOptions->set_IgnoreHeaderFooter(false);

dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, importFormatOptions);

dstDoc->Save(get_ArtifactsDir() + u"DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
