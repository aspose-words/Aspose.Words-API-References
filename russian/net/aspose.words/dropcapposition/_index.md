---
title: Enum DropCapPosition
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.DropCapPosition перечисление. Определяет положение текста буквицы.
type: docs
weight: 1260
url: /ru/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Определяет положение текста буквицы.

```csharp
public enum DropCapPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Абзац не имеет буквицы. |
| Normal | `1` | Буквица расположена внутри текстового поля анкорного абзаца. |
| Margin | `2` | Буквица расположена за пределами поля текста в абзаце привязки. |

### Примеры

Показывает, как создать буквицу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставить один абзац с большой буквы, с которой начинается текст во втором и третьем абзацах.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// В настоящее время второй и третий абзацы будут отображаться под первым.
// Мы можем преобразовать первый абзац в качестве буквицы для других абзацев через его объект «ParagraphFormat».
// Установите для свойства "DropCapPosition" значение "DropCapPosition.Margin", чтобы разместить буквицу
// вне левого поля страницы, если наш текст написан слева направо.
// Установите для свойства "DropCapPosition" значение "DropCapPosition.Normal", чтобы разместить буквицу на полях страницы
// и обернуть вокруг него остальную часть текста.
// «DropCapPosition.None» — это состояние по умолчанию для всех абзацев.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


