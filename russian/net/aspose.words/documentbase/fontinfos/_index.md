---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words для .NET
description: Получите доступ к подробным свойствам шрифта с помощью функции FontInfos DocumentBase, которая позволит без труда улучшить дизайн и читабельность вашего документа.
type: docs
weight: 30
url: /ru/net/aspose.words/documentbase/fontinfos/
---
## DocumentBase.FontInfos property

Предоставляет доступ к свойствам шрифтов, используемых в этом документе.

```csharp
public FontInfoCollection FontInfos { get; }
```

## Примечания

Эта коллекция определений шрифтов загружается из документа «как есть». Определения шрифтов могут быть необязательными, отсутствующими или неполными в некоторых документах.

Не полагайтесь на эту коллекцию, чтобы убедиться, что в документе используется определенный шрифт. Эту коллекцию следует использовать только для получения информации о шрифтах, которые могут использоваться в документе.

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

Показывает, как распечатать подробную информацию о шрифтах, присутствующих в документе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Распечатать все используемые и неиспользуемые шрифты в документе.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

### Смотрите также

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
