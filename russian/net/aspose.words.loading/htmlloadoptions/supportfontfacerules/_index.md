---
title: HtmlLoadOptions.SupportFontFaceRules
linktitle: SupportFontFaceRules
articleTitle: SupportFontFaceRules
second_title: Aspose.Words для .NET
description: Откройте для себя HtmlLoadOptions SupportFontFaceRules, легко управляйте загрузкой шрифтов. Улучшите свой веб-дизайн, включив пользовательские шрифты для изысканного вида.
type: docs
weight: 60
url: /ru/net/aspose.words.loading/htmlloadoptions/supportfontfacerules/
---
## HtmlLoadOptions.SupportFontFaceRules property

Возвращает или задает значение, указывающее, следует ли поддерживать правила @font-face и загружать ли объявленные шрифты. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool SupportFontFaceRules { get; set; }
```

## Примечания

Если эта опция включена, шрифты, объявленные в правилах @font-face, загружаются и внедряются в определения шрифтов результирующего документа (см.[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) ). Это делает загруженные шрифты доступными для рендеринга, но не включает автоматическое внедрение шрифтов при сохранении. Чтобы сохранить документ с загруженными шрифтами, [`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) собственность[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) Коллекция должна быть установлена на`истинный` .

Поддерживаемые форматы шрифтов: TTF, EOT и WOFF.

Правила @font-face не поддерживаются при загрузке изображений SVG.

## Примеры

Показывает, как загрузить объявленные правила «@font-face».

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();
loadOptions.SupportFontFaceRules = true;
Document doc = new Document(MyDir + "Html with FontFace.html", loadOptions);

Assert.AreEqual("Squarish Sans CT Regular", doc.FontInfos[0].Name);
```

### Смотрите также

* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
