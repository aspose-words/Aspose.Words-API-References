---
title: Enum RevisionColor
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Layout.RevisionColor перечисление. Позволяет указать цвет редакций документа.
type: docs
weight: 3380
url: /ru/net/aspose.words.layout/revisioncolor/
---
## RevisionColor enumeration

Позволяет указать цвет редакций документа.

```csharp
public enum RevisionColor
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | По умолчанию. |
| Black | `1` | Представляет цвет 000000. |
| Blue | `2` | Представляет цвет 2e97d3. |
| BrightGreen | `3` | Представляет цвет 84a35b. |
| ClassicBlue | `4` | Представляет цвет 0000ff. |
| ClassicRed | `5` | Представляет цвет ff0000. |
| DarkBlue | `6` | Представляет цвет 376e96. |
| DarkRed | `7` | Представляет 881824 цвета. |
| DarkYellow | `8` | Представляет цвет e09a2b. |
| Gray25 | `9` | Представляет цвет a0a3a9. |
| Gray50 | `10` | Представляет цвет 50565e. |
| Green | `11` | Представляет цвет 2c6234. |
| Pink | `12` | Представляет цвет ce338f. |
| Red | `13` | Представляет цвет b5082e. |
| Teal | `14` | Представляет цвет кабины 1b9. |
| Turquoise | `15` | Представляет цвет 3eafc2. |
| Violet | `16` | Представляет 633277 цветов. |
| White | `17` | Представляет цвет ffffff. |
| Yellow | `18` | Представляет цвет fad272. |
| NoHighlight | `19` | Для выделения изменений версии цвет не используется. |
| ByAuthor | `20` | Редакции каждого автора получают свой цвет для выделения из заранее заданного набора высококонтрастных цветов. |

### Примеры

Показывает, как изменить внешний вид редакций в готовом к просмотру выходном документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем ревизию, затем меняем цвет всех ревизий на зеленый.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Удалить полосу, которая появляется слева от каждой измененной строки.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)


