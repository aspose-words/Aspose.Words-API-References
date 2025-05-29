---
title: FontInfo Class
linktitle: FontInfo
articleTitle: FontInfo
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.FontInfo — ваш ключ к подробному анализу шрифтов в документах, повышению качества текста и визуальной привлекательности.
type: docs
weight: 3350
url: /ru/net/aspose.words.fonts/fontinfo/
---
## FontInfo class

Указывает информацию о шрифте, используемом в документе.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FontInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [AltName](../../aspose.words.fonts/fontinfo/altname/) { get; set; } | Получает или задает альтернативное имя для шрифта. |
| [Charset](../../aspose.words.fonts/fontinfo/charset/) { get; set; } | Получает или задает набор символов для шрифта. |
| [EmbeddingLicensingRights](../../aspose.words.fonts/fontinfo/embeddinglicensingrights/) { get; } | Получает права лицензирования встроенного шрифта. |
| [Family](../../aspose.words.fonts/fontinfo/family/) { get; set; } | Возвращает или задает семейство шрифтов, к которому принадлежит этот шрифт. |
| [IsTrueType](../../aspose.words.fonts/fontinfo/istruetype/) { get; set; } | Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию:`истинный` . |
| [Name](../../aspose.words.fonts/fontinfo/name/) { get; } | Получает имя шрифта. |
| [Panose](../../aspose.words.fonts/fontinfo/panose/) { get; set; } | Возвращает или задает номер классификации шрифта PANOSE. |
| [Pitch](../../aspose.words.fonts/fontinfo/pitch/) { get; set; } | Шаг указывает, является ли шаг шрифта фиксированным, пропорциональным или полагается на настройки по умолчанию. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEmbeddedFont](../../aspose.words.fonts/fontinfo/getembeddedfont/)(*[EmbeddedFontFormat](../embeddedfontformat/), [EmbeddedFontStyle](../embeddedfontstyle/)*) | Получает определенный встроенный файл шрифта. |
| [GetEmbeddedFontAsOpenType](../../aspose.words.fonts/fontinfo/getembeddedfontasopentype/)(*[EmbeddedFontStyle](../embeddedfontstyle/)*) | Получает файл встроенного шрифта в формате OpenType. Шрифты в формате Embedded OpenType преобразуются в OpenType. |

## Примечания

Вы не создаете экземпляры этого класса напрямую. Используйте[`FontInfos`](../../aspose.words/documentbase/fontinfos/) свойство для доступа к коллекции fonts , определенной в документе.

## Примеры

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

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
