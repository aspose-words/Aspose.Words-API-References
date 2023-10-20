---
title: ShowInBalloons Enum
linktitle: ShowInBalloons
articleTitle: ShowInBalloons
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.ShowInBalloons перечисление. Указывает какие версии отображаются в выносках на С#.
type: docs
weight: 3410
url: /ru/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

Указывает, какие версии отображаются в выносках.

```csharp
public enum ShowInBalloons
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Вставляет, удаляет и форматирует ревизии в режиме реального времени. |
| Format | `1` | Отображает вставку и удаление редакций встроенными, форматирует ревизии в выносках. |
| FormatAndDelete | `2` | Отображает вставку редакций встроенными, удаление и форматирование редакций в выносках. |

## Примечания

Обратите внимание, что изменения не отображаются в выносках дляShowInAnnotations .

## Примеры

Показывает, как изменить внешний вид редакций.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Получаем объект RevisionOptions, который управляет внешним видом редакций.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Отображение изменений вставки зеленым и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Отобразить удаленные версии красным и жирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Один и тот же текст появится дважды в версии движения:
// один раз в пункте отправления и один раз в пункте назначения.
// Отобразить текст в перенесенной из редакции желтого цвета с двойным перечеркиванием
// и двойное подчеркивание синим цветом в перенесенной версии.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Редакции формата отображаются темно-красным и жирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Размещаем толстую темно-синюю полосу в левой части страницы рядом со строками, на которые внесены изменения.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Показать отметки редакции и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Получение перемещения, удаления, изменений форматирования и комментариев, которые будут отображаться в зеленых выносках
// в правой части страницы.
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// Эти функции применимы только к таким форматам, как .pdf или .jpg.
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
