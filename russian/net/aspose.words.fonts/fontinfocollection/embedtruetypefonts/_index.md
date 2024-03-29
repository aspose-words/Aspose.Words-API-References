---
title: FontInfoCollection.EmbedTrueTypeFonts
linktitle: EmbedTrueTypeFonts
articleTitle: EmbedTrueTypeFonts
second_title: Aspose.Words для .NET
description: FontInfoCollection EmbedTrueTypeFonts свойство. Указывает следует ли встраивать шрифты TrueType в документ при его сохранении. Значение по умолчанию для этого свойстваЛОЖЬ  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/fontinfocollection/embedtruetypefonts/
---
## FontInfoCollection.EmbedTrueTypeFonts property

Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. Значение по умолчанию для этого свойства:`ЛОЖЬ` .

```csharp
public bool EmbedTrueTypeFonts { get; set; }
```

## Примечания

Встраивание шрифтов TrueType позволяет другим просматривать документ с теми же шрифтами, которые использовались для его создания, , но может существенно увеличить размер документа.

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

if (embedAllFonts)
    Assert.That(25000, Is.LessThan(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
else
    Assert.That(15000, Is.AtLeast(new FileInfo(ArtifactsDir + "Font.FontInfoCollection.docx").Length));
```

### Смотрите также

* class [FontInfoCollection](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
