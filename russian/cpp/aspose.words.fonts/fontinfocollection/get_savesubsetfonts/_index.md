---
title: "Метод Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts"
linktitle: "get_SaveSubsetFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts. Указывает, следует ли сохранять подмножество встроенных TrueType шрифтов в документе. Значение по умолчанию для этого свойства — false. Эта опция работает только когда свойство EmbedTrueTypeFonts установлено в true в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Указывает, следует ли сохранять подмножество встроенных TrueType шрифтов в документе. Значение по умолчанию для этого свойства — **false**. Эта опция работает только когда свойство [EmbedTrueTypeFonts](../get_embedtruetypefonts/) установлено в **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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
