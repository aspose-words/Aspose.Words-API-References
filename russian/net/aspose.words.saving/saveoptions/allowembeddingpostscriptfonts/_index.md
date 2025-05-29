---
title: SaveOptions.AllowEmbeddingPostScriptFonts
linktitle: AllowEmbeddingPostScriptFonts
articleTitle: AllowEmbeddingPostScriptFonts
second_title: Aspose.Words для .NET
description: Управляйте внедрением шрифтов в ваши документы с помощью SaveOptions' AllowEmbeddingPostScriptFonts. Легко управляйте параметрами шрифтов TrueType для повышения качества документов.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/
---
## SaveOptions.AllowEmbeddingPostScriptFonts property

Возвращает или задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ при его сохранении. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool AllowEmbeddingPostScriptFonts { get; set; }
```

## Примечания

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

Эта опция работает только тогда, когда[`EmbedTrueTypeFonts`](../../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) из x000d_[`FontInfos`](../../../aspose.words/documentbase/fontinfos/) свойство установлено на`истинный`.

## Примеры

Показывает, как сохранить документ со шрифтом PostScript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "PostScriptFont";
builder.Writeln("Some text with PostScript font.");

// Загружаем шрифт PostScript для использования в документе.
MemoryFontSource otf = new MemoryFontSource(File.ReadAllBytes(FontsDir + "AllegroOpen.otf"));
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] { otf });

// Внедрение шрифтов TrueType.
doc.FontInfos.EmbedTrueTypeFonts = true;

// Разрешить встраивание шрифтов PostScript при встраивании шрифтов TrueType.
// Microsoft Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Docx);
saveOptions.AllowEmbeddingPostScriptFonts = true;

doc.Save(ArtifactsDir + "Document.AllowEmbeddingPostScriptFonts.docx", saveOptions);
```

### Смотрите также

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
