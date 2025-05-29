---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.OutlineLevel, которое поможет вам легко управлять уровнями структуры абзацев в документах для лучшей организации и ясности.
type: docs
weight: 5060
url: /ru/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Указывает уровень структуры абзаца в документе.

```csharp
public enum OutlineLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Level1 | `0` | Абзац находится на уровне структуры 1 (самый верхний уровень). |
| Level2 | `1` | Абзац находится на уровне структуры 2. |
| Level3 | `2` | Абзац находится на уровне структуры 3. |
| Level4 | `3` | Абзац находится на уровне структуры 4. |
| Level5 | `4` | Абзац находится на уровне структуры 5. |
| Level6 | `5` | Абзац находится на уровне структуры 6. |
| Level7 | `6` | Абзац находится на уровне структуры 7. |
| Level8 | `7` | Абзац находится на уровне структуры 8. |
| Level9 | `8` | Абзац находится на уровне структуры 9. |
| BodyText | `9` | Абзац находится на уровне основного текста. |

## Примеры

Показывает, как настроить уровни структуры абзаца для создания сворачиваемого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац имеет OutlineLevel, который может быть любым числом от 1 до 9 или иметь значение по умолчанию «BodyText».
// Установка свойства в одно из пронумерованных значений отобразит стрелку влево
// начала абзаца.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Уровень 1 — самый верхний уровень. Если есть абзац с более низким уровнем под абзацем с более высоким уровнем,
// сворачивание абзаца более высокого уровня приведет к сворачиванию абзаца более низкого уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Два абзаца одного уровня не будут сворачивать друг друга,
// и стрелки не сворачивают абзацы, на которые они указывают.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Значение "BodyText" по умолчанию — наименьшее, при котором абзац любого уровня может свернуться.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
