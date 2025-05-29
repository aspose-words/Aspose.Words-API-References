---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Fonts.FontFamily — ваш ключ к легкому управлению разнообразными семействами шрифтов для улучшенного оформления и форматирования документов.
type: docs
weight: 3340
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
| Auto | `0` | Указывает общее имя семейства. Это имя используется, когда информация о шрифте отсутствует или не имеет значения. Используется шрифт по умолчанию. |
| Roman | `1` | Указывает пропорциональный шрифт с засечками. Пример — Times New Roman. |
| Swiss | `2` | Указывает пропорциональный шрифт без засечек. Пример — Arial. |
| Modern | `3` | Указывает моноширинный шрифт с засечками или без них. Моноширинные шрифты обычно современные; примеры включают Pica, Elite и Courier New. |
| Script | `4` | Указывает шрифт, который выглядит как рукописный; примеры включают Script и Cursive. |
| Decorative | `5` | Указывает новый шрифт. Пример — Old English. |

## Примечания

Семейство шрифтов — это набор шрифтов, имеющих общую ширину штрихов и характеристики засечек.

## Примеры

Показывает, как получить доступ к сведениям о каждом шрифте в документе и распечатать их.

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Альтернативные имена обычно пустые.
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
