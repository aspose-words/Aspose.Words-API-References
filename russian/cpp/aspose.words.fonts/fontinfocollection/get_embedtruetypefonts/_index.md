---
title: "Метод Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts. Указывает, следует ли встраивать TrueType шрифты в документ при его сохранении. Значение по умолчанию для этого свойства — false в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Указывает, следует ли встраивать TrueType шрифты в документ при сохранении. Значение по умолчанию для этого свойства — **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Примечания


Встраивание TrueType шрифтов позволяет другим просматривать документ с теми же шрифтами, которые использовались при его создании, но может существенно увеличить размер документа.

Эта опция работает только с форматами DOC, DOCX и RTF.

## Примеры



Показывает, как сохранить документ со встроенными TrueType шрифтами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## См. также

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
