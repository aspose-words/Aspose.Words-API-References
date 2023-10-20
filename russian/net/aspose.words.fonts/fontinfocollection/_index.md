---
title: FontInfoCollection Class
linktitle: FontInfoCollection
articleTitle: FontInfoCollection
second_title: Aspose.Words для .NET
description: Aspose.Words.Fonts.FontInfoCollection сорт. Представляет коллекцию шрифтов используемых в документе на С#.
type: docs
weight: 2930
url: /ru/net/aspose.words.fonts/fontinfocollection/
---
## FontInfoCollection class

Представляет коллекцию шрифтов, используемых в документе.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class FontInfoCollection : IEnumerable<FontInfo>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.fonts/fontinfocollection/count/) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [EmbedSystemFonts](../../aspose.words.fonts/fontinfocollection/embedsystemfonts/) { get; set; } | Указывает, следует ли встраивать системные шрифты в документ. Значение по умолчанию для этого свойства:`ЛОЖЬ`. |
| [EmbedTrueTypeFonts](../../aspose.words.fonts/fontinfocollection/embedtruetypefonts/) { get; set; } | Указывает, следует ли встраивать шрифты TrueType в документ при его сохранении. Значение по умолчанию для этого свойства:`ЛОЖЬ` . |
| [Item](../../aspose.words.fonts/fontinfocollection/item/) { get; } | Получает шрифт с указанным именем. (2 indexers) |
| [SaveSubsetFonts](../../aspose.words.fonts/fontinfocollection/savesubsetfonts/) { get; set; } | Указывает, следует ли сохранять подмножество встроенных шрифтов TrueType вместе с документом. Значение по умолчанию для этого свойства:`ЛОЖЬ`. |

## Методы

| Имя | Описание |
| --- | --- |
| [Contains](../../aspose.words.fonts/fontinfocollection/contains/)(*string*) | Определяет, содержит ли коллекция шрифт с данным именем. |
| [GetEnumerator](../../aspose.words.fonts/fontinfocollection/getenumerator/)() | Возвращает объект перечислителя, который можно использовать для перебора всех элементов коллекции. |

## Примечания

Предметы[`FontInfo`](../fontinfo/) объекты.

Вы не создаете экземпляры этого класса напрямую. Используйте[`FontInfos`](../../aspose.words/documentbase/fontinfos/) свойство для доступа к коллекции шрифтов , определенной в документе.

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

* class [FontInfo](../fontinfo/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
