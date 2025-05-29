---
title: FontInfo.GetEmbeddedFont
linktitle: GetEmbeddedFont
articleTitle: GetEmbeddedFont
second_title: Aspose.Words для .NET
description: Откройте для себя метод FontInfo GetEmbeddedFont, позволяющий легко извлекать определенные файлы встроенных шрифтов и улучшать свои дизайн-проекты с помощью бесшовной типографики.
type: docs
weight: 90
url: /ru/net/aspose.words.fonts/fontinfo/getembeddedfont/
---
## FontInfo.GetEmbeddedFont method

Получает определенный встроенный файл шрифта.

```csharp
public byte[] GetEmbeddedFont(EmbeddedFontFormat format, EmbeddedFontStyle style)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| format | EmbeddedFontFormat | Указывает формат шрифта для извлечения. |
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

* enum [EmbeddedFontFormat](../../embeddedfontformat/)
* enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* class [FontInfo](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
