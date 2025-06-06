---
title: FontPitch Enum
linktitle: FontPitch
articleTitle: FontPitch
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Fonts.FontPitch — мощный инструмент для управления стилями шрифтов и улучшения форматирования документов в ваших приложениях.
type: docs
weight: 3390
url: /ru/net/aspose.words.fonts/fontpitch/
---
## FontPitch enumeration

Представляет шаг шрифта.

```csharp
public enum FontPitch
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Default | `0` | Указывает, что информация о высоте шрифта отсутствует. |
| Fixed | `1` | Указывает, что это шрифт фиксированной ширины. |
| Variable | `2` | Указывает, что это шрифт пропорциональной ширины. |

## Примечания

Шаг указывает, имеет ли шрифт фиксированный шаг, пропорциональный интервал или использует настройки по умолчанию.

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
