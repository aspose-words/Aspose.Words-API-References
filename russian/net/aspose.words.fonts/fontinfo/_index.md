---
title: Class FontInfo
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.FontInfo сорт. Указывает информацию о шрифте используемом в документе.
type: docs
weight: 2920
url: /ru/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Указывает информацию о шрифте, используемом в документе.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class FontInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Получает или задает альтернативное имя шрифта. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Получает или задает набор символов для шрифта. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Получает или задает семейство шрифтов, к которому принадлежит этот шрифт. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию:`истинный` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Получает имя шрифта. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Получает или задает классификационный номер шрифта PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Шаг указывает, является ли шрифт фиксированным, пропорциональным или основан на настройке по умолчанию. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(EmbeddedFontFormat, EmbeddedFontStyle) | Получает определенный файл встроенного шрифта. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(EmbeddedFontStyle) | Получает файл встроенного шрифта в формате OpenType. Шрифты в формате Embedded OpenType преобразуются в OpenType. . |

### Примечания

Вы не создаете экземпляры этого класса напрямую. Используйте[`FontInfos`](../../aspose.words/documentbase/fontinfos/) свойство для доступа к коллекции шрифтов , определенной в документе.

### Примеры

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

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


