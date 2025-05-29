---
title: RevisionColor Enum
linktitle: RevisionColor
articleTitle: RevisionColor
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Layout.RevisionColor для настройки цветов редакций документов, повышения ясности и улучшения совместной работы над документами.
type: docs
weight: 3830
url: /ru/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Позволяет указать цвет ревизий документа.

```csharp
public enum RevisionColor
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | По умолчанию. |
| Black | `1` | Представляет 000000 цвет. |
| Blue | `2` | Представляет цвет 2e97d3. |
| BrightGreen | `3` | Представляет цвет 84a35b. |
| ClassicBlue | `4` | Представляет цвет 0000ff. |
| ClassicRed | `5` | Представляет цвет ff0000. |
| DarkBlue | `6` | Представляет 376e96 цвет. |
| DarkRed | `7` | Представляет 881824 цвета. |
| DarkYellow | `8` | Представляет цвет e09a2b. |
| Gray25 | `9` | Представляет цвет a0a3a9. |
| Gray50 | `10` | Представляет цвет 50565e. |
| Green | `11` | Представляет цвет 2c6234. |
| Pink | `12` | Представляет цвет ce338f. |
| Red | `13` | Представляет цвет b5082e. |
| Teal | `14` | Представляет цвет 1b9cab. |
| Turquoise | `15` | Представляет цвет 3eafc2. |
| Violet | `16` | Представляет 633277 цветов. |
| White | `17` | Представляет цвет ffffff. |
| Yellow | `18` | Представляет цвет fad272. |
| LightPink | `19` | Представляет цвет fce6f4. |
| LightBlue | `20` | Представляет цвет e1f2fa. |
| LightYellow | `21` | Представляет цвет fef4de. |
| LightPurple | `22` | Представляет цвет eadfef. |
| LightOrange | `23` | Представляет цвет fce3d0. |
| LightGreen | `24` | Представляет цвет e9f8ce. |
| Gray | `25` | Представляет цвет efeded. |
| NoHighlight | `26` | Для выделения изменений в ревизии цвет не используется. |
| ByAuthor | `27` | Редакции каждого автора получают свой собственный цвет для выделения из предопределенного набора высококонтрастных цветов. |

## Примеры

Показывает, как изменить внешний вид изменений в визуализированном выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте ревизию, затем измените цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
