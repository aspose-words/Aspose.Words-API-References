---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words для .NET
description: Узнайте, как свойство EmbedTrueTypeFonts в FontInfoCollection улучшает качество документа, позволяя внедрять шрифты TrueType. Значение по умолчанию — false.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. Значение этого свойства по умолчанию:`ЛОЖЬ` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Примечания

Внедрение шрифтов TrueType позволяет другим просматривать документ с теми же шрифтами, которые использовались при его создании, , но может существенно увеличить размер документа.

Эта опция работает только для форматов DOC, DOCX и RTF.

## Примеры

Показывает, как сохранить документ со встроенными шрифтами TrueType.

```csharp
Document doc = new Document(MyDir + "Document.docx");

FontInfoCollection fontInfos = doc.FontInfos;
fontInfos.EmbedTrueTypeFonts = embedAllFonts;
fontInfos.EmbedSystemFonts = embedAllFonts;
fontInfos.SaveSubsetFonts = embedAllFonts;

doc.Save(ArtifactsDir + "Font.FontInfoCollection.docx");
```

### Смотрите также

* class [FontInfoCollection](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
