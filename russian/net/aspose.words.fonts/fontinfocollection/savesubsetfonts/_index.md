---
title: FontInfoCollection.SaveSubsetFonts
linktitle: SaveSubsetFonts
articleTitle: SaveSubsetFonts
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontInfoCollection SaveSubsetFonts, управляйте встроенными подмножествами шрифтов TrueType в ваших документах для оптимизации размера файла и производительности.
type: docs
weight: 50
url: /ru/net/aspose.words.fonts/fontinfocollection/savesubsetfonts/
---
## FontInfoCollection.SaveSubsetFonts property

Указывает, следует ли сохранять подмножество встроенных шрифтов TrueType вместе с документом. Значение этого свойства по умолчанию:`ЛОЖЬ`.

Эта опция работает только тогда, когда[`EmbedTrueTypeFonts`](../embedtruetypefonts/) свойство установлено на`истинный`.

```csharp
public bool SaveSubsetFonts { get; set; }
```

## Примечания

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
