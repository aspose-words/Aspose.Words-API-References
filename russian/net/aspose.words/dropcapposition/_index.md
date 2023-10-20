---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words для .NET
description: Aspose.Words.DropCapPosition перечисление. Определяет положение текста буквицы на С#.
type: docs
weight: 1410
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
| None | `0` | В абзаце нет буквицы. |
| Normal | `1` | Буквица располагается внутри поля текста привязки абзаца. |
| Margin | `2` | Буквица расположена за пределами поля текста в привязном абзаце. |

## Примеры

Показывает, как создать буквицу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем один абзац с большой буквы, с которой начинается текст во втором и третьем абзацах.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// В настоящее время второй и третий абзацы появятся под первым.
// Мы можем преобразовать первый абзац в буквицу для остальных абзацев через его объект «ParagraphFormat».
// Установите для свойства «DropCapPosition» значение «DropCapPosition.Margin», чтобы разместить буквицу
// за пределами левого поля страницы, если наш текст идет слева направо.
// Установите для свойства DropCapPosition значение DropCapPosition.Normal, чтобы разместить буквицу на полях страницы.
// и обернуть вокруг него остальной текст.
// «DropCapPosition.None» — это состояние по умолчанию для всех абзацев.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
