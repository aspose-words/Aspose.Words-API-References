---
title: "Aspose::Words::DocumentBase::get_FontInfos метод"
linktitle: "get_FontInfos"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_FontInfos метод. Предоставляет доступ к свойствам шрифтов, используемых в этом документе, в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Обеспечивает доступ к свойствам шрифтов, используемых в этом документе.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Примечания


Эта коллекция определений шрифтов загружается из документа без изменений. Определения [Font](../../font/) могут быть необязательными, отсутствовать или быть неполными в некоторых документах.

Не полагайтесь на эту коллекцию, чтобы определить, используется ли конкретный шрифт в документе. Вы должны использовать эту коллекцию только для получения информации о шрифтах, которые могут использоваться в документе.

## Примеры



Показывает, как вывести детали о шрифтах, присутствующих в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Вывести все используемые и неиспользуемые шрифты в документе.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
