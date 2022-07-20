---
title: SaveSubsetFonts
second_title: Справочник по API Aspose.Words для .NET
description: Указывает следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. Значение по умолчанию для этого свойства ЛОЖЬ.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Указывает, следует ли сохранять вместе с документом подмножество встроенных шрифтов TrueType. Значение по умолчанию для этого свойства: **ЛОЖЬ**.

Этот вариант работает только тогда, когда[`EmbedTrueTypeFonts`](../embedtruetypefonts) свойство установлено на **истинный**.

```csharp
public bool SaveSubsetFonts { get; set; }
```

### Примечания

Эта опция работает только для форматов DOC, DOCX и RTF.

### Примеры

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

* class [FontInfoCollection](../../fontinfocollection)
* пространство имен [Aspose.Words.Fonts](../../fontinfocollection)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->