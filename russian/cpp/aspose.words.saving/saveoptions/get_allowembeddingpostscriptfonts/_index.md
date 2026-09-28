---
title: "метод Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts"
linktitle: "get_AllowEmbeddingPostScriptFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts. Получает или задает логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType шрифтов в документ при его сохранении. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/saveoptions/get_allowembeddingpostscriptfonts/
---
## SaveOptions::get_AllowEmbeddingPostScriptFonts method


Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts() const
```

## Примечания


Обратите внимание, Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

Эта опция работает только когда свойство [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) у [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) установлено в **true**.

## Примеры



Показывает, как сохранить документ с шрифтом PostScript.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"PostScriptFont");
builder->Writeln(u"Some text with PostScript font.");

// Загрузите шрифт с PostScript для использования в документе.
auto otf = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(System::IO::File::ReadAllBytes(get_FontsDir() + u"AllegroOpen.otf"));
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({otf}));

// Встроить TrueType шрифты.
doc->get_FontInfos()->set_EmbedTrueTypeFonts(true);

// Разрешить встраивание шрифтов PostScript при встраивании TrueType шрифтов.
// Microsoft Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat::Docx);
saveOptions->set_AllowEmbeddingPostScriptFonts(true);

doc->Save(get_ArtifactsDir() + u"Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

## См. также

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
