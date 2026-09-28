---
title: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules"
linktitle: "get_SupportFontFaceRules"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules. Получает или задает значение, указывающее, поддерживать ли правила @font-face и загружать ли объявленные шрифты. Значение по умолчанию — false в C++."
type: docs
weight: 6500
url: /ru/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


Получает или задает значение, указывающее, поддерживать ли правила @font-face и загружать объявленные шрифты. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## Примечания


Если эта опция включена, шрифты, объявленные в правилах @font-face, загружаются и встраиваются в определения шрифтов получаемого документа (см. [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). Это делает загруженные шрифты доступными для рендеринга, но не включает автоматическое встраивание шрифтов при сохранении. Чтобы сохранить документ с загруженными шрифтами, свойство [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) коллекции [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) должно быть установлено в **true**.

Поддерживаемые форматы шрифтов: TTF, EOT и WOFF.

Правила @font-face не поддерживаются при загрузке SVG‑изображений.

## Примеры



Показывает, как загружать объявленные правила "@font-face".
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## См. также

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
