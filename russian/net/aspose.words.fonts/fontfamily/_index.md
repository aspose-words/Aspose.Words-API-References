---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words для .NET
description: Aspose.Words.Fonts.FontFamily перечисление. Представляет семейство шрифтов на С#.
type: docs
weight: 2910
url: /ru/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

Представляет семейство шрифтов.

```csharp
public enum FontFamily
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Указывает общее имя семейства. Это имя используется, когда информация о шрифте не существует или не имеет значения. Используется шрифт по умолчанию. . |
| Roman | `1` | Определяет пропорциональный шрифт с засечками. Примером является Times New Roman. . |
| Swiss | `2` | Определяет пропорциональный шрифт без засечек. Пример: Arial. . |
| Modern | `3` | Определяет моноширинный шрифт с засечками или без них. Моноширинные шрифты обычно современные; примеры включают Pica, Elite и Courier New. . |
| Script | `4` | Определяет шрифт, похожий на рукописный; примеры включают Script и Cursive. . |
| Decorative | `5` | Указывает новый шрифт. Примером является древнеанглийский. . |

## Примечания

Семейство шрифтов — это набор шрифтов, имеющих общую ширину штриха и характеристики засечек.

## Примеры

Показывает, как получить доступ и распечатать сведения о каждом шрифте в документе.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Альтернативные имена обычно пусты.
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
