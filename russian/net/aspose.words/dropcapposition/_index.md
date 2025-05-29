---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.DropCapPosition, чтобы улучшить дизайн документа, определив уникальные позиции текста буквицы для создания впечатляющего визуального эффекта.
type: docs
weight: 1820
url: /ru/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Указывает положение текста буквицы.

```csharp
public enum DropCapPosition
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | В абзаце нет буквицы. |
| Normal | `1` | Буквица располагается внутри текстового поля в абзаце привязки. |
| Margin | `2` | Буквица расположена за пределами текстового поля в абзаце привязки. |

## Примеры

Показывает, как создать буквицу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте один абзац с большой буквы, с которой начинается текст во втором и третьем абзацах.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// В настоящее время второй и третий абзацы будут отображаться под первым.
// Мы можем преобразовать первый абзац в буквицу для других абзацев с помощью его объекта «ParagraphFormat».
// Установите свойство "DropCapPosition" на "DropCapPosition.Margin", чтобы разместить буквицу
// за пределами левого поля страницы, если наш текст написан слева направо.
// Установите свойство "DropCapPosition" на "DropCapPosition.Normal", чтобы разместить буквицу в пределах полей страницы
// и обернуть вокруг него остальной текст.
// "DropCapPosition.None" — состояние по умолчанию для всех абзацев.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
