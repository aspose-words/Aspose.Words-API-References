---
title: FontInfo.IsTrueType
second_title: Справочник по API Aspose.Words для .NET
description: FontInfo свойство. Указывает что этот шрифт является шрифтом TrueType или OpenType а не растровым или векторным шрифтом. Значение по умолчаниюистинный .
type: docs
weight: 40
url: /ru/net/aspose.words.fonts/fontinfo/istruetype/
---
## FontInfo.IsTrueType property

Указывает, что этот шрифт является шрифтом TrueType или OpenType, а не растровым или векторным шрифтом. Значение по умолчанию:`истинный` .

```csharp
public bool IsTrueType { get; set; }
```

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

* class [FontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../fontinfo/)
* сборка [Aspose.Words](../../../)


