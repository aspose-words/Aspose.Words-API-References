---
title: "Метод Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts"
linktitle: "get_EmbedSystemFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts. Указывает, следует ли встраивать системные шрифты в документ. Значение по умолчанию для этого свойства — false. Эта опция работает только когда параметр EmbedTrueTypeFonts установлен в true в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Указывает, следует ли встраивать системные шрифты в документ. Значение по умолчанию для этого свойства — **false**. Эта опция работает только когда параметр [EmbedTrueTypeFonts](../get_embedtruetypefonts/) установлен в **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Примечания


Установка этого свойства в **true** полезна, если пользователь работает на системе Восточной Азии и хочет создать документ, читаемый другими, у которых нет шрифтов для этого языка. Например, пользователь на японской системе может выбрать встраивание шрифтов в документ, чтобы японский документ был читаем на всех системах.

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
