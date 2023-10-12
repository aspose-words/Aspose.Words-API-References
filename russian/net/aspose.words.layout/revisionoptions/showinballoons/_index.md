---
title: RevisionOptions.ShowInBalloons
second_title: Справочник по API Aspose.Words для .NET
description: RevisionOptions свойство. Позволяет указать отображаются ли изменения в выносках. Значение по умолчаниюNone .
type: docs
weight: 160
url: /ru/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Позволяет указать, отображаются ли изменения в выносках. Значение по умолчанию:None .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### Примечания

Обратите внимание, что изменения не отображаются в выносках дляShowInAnnotations .

### Примеры

Показывает, как отображать изменения в выносках.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// По умолчанию текст, являющийся редакцией, имеет другой цвет, чтобы отличать его от другого текста, не являющегося редакцией.
// Установите параметр редакции, чтобы отображать более подробную информацию о каждой редакции в выноске на правом поле страницы.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

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

* enum [ShowInBalloons](../../showinballoons/)
* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../revisionoptions/)
* сборка [Aspose.Words](../../../)


