---
title: DocumentBase.FontInfos
linktitle: FontInfos
articleTitle: FontInfos
second_title: Aspose.Words для .NET
description: DocumentBase FontInfos свойство. Предоставляет доступ к свойствам шрифтов используемых в этом документе на С#.
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

Эта коллекция определений шрифтов загружается в том виде, в каком она есть из документа. В некоторых документах определения шрифтов могут быть необязательными, отсутствовать или быть неполными.

Не полагайтесь на эту коллекцию, чтобы убедиться, что в документе используется определенный шрифт. Эту коллекцию следует использовать только для получения информации о шрифтах, которые могут использоваться в документе.

## Примеры

Показывает, как распечатать сведения о том, какие шрифты присутствуют в документе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfoCollection allFonts = doc.FontInfos;
// Распечатываем все использованные и неиспользуемые шрифты в документе.
for (int i = 0; i < allFonts.Count; i++)
{
    Console.WriteLine($"Font index #{i}");
    Console.WriteLine($"\tName: {allFonts[i].Name}");
    Console.WriteLine($"\tIs {(allFonts[i].IsTrueType ? "" : "not ")}a trueType font");
}
```

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

* class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
