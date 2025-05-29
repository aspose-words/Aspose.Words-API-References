---
title: FontInfo.GetEmbeddedFontAsOpenType
linktitle: GetEmbeddedFontAsOpenType
articleTitle: GetEmbeddedFontAsOpenType
second_title: Aspose.Words для .NET
description: Узнайте, как метод FontInfo GetEmbeddedFontAsOpenType извлекает встроенные шрифты в формате OpenType, повышая гибкость и качество вашего дизайна.
type: docs
weight: 100
url: /ru/net/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo.GetEmbeddedFontAsOpenType method

Получает файл встроенного шрифта в формате OpenType. Шрифты в формате Embedded OpenType преобразуются в OpenType.

```csharp
public byte[] GetEmbeddedFontAsOpenType(EmbeddedFontStyle style)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| style | EmbeddedFontStyle | Указывает стиль шрифта для извлечения. |

### Возвращаемое значение

Возвраты`нулевой` если указанный шрифт не встроен.

## Примеры

Показывает, как извлечь встроенный шрифт из документа и сохранить его в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

FontInfo embeddedFont = doc.FontInfos["Alte DIN 1451 Mittelschrift"];
byte[] embeddedFontBytes = embeddedFont.GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular);
File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Форматы встроенных шрифтов могут отличаться в других форматах, таких как .doc.
// Прежде чем извлечь шрифт, нам нужно знать правильный формат.
doc = new Document(MyDir + "Embedded font.doc");

Assert.IsNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.OpenType, EmbeddedFontStyle.Regular));
Assert.IsNotNull(doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFont(EmbeddedFontFormat.EmbeddedOpenType, EmbeddedFontStyle.Regular));

// Кроме того, мы можем преобразовать встроенный формат OpenType, который получен из документов .doc, в OpenType.
embeddedFontBytes = doc.FontInfos["Alte DIN 1451 Mittelschrift"].GetEmbeddedFontAsOpenType(EmbeddedFontStyle.Regular);

File.WriteAllBytes(ArtifactsDir + "Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

### Смотрите также

* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
