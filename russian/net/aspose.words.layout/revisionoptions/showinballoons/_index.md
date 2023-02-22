---
title: RevisionOptions.ShowInBalloons
second_title: Справочник по API Aspose.Words для .NET
description: RevisionOptions свойство. Позволяет указать будут ли ревизии отображаться во всплывающих подсказках. Значение по умолчаниюNone .
type: docs
weight: 160
url: /ru/net/aspose.words.layout/revisionoptions/showinballoons/
---
## RevisionOptions.ShowInBalloons property

Позволяет указать, будут ли ревизии отображаться во всплывающих подсказках. Значение по умолчанию:None .

```csharp
public ShowInBalloons ShowInBalloons { get; set; }
```

### Примечания

Обратите внимание, что ревизии не отображаются во всплывающих подсказках дляShowInAnnotations .

### Примеры

Показывает, как отображать версии во всплывающих подсказках.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// По умолчанию текст, который является исправлением, имеет другой цвет, чтобы отличить его от другого текста, не являющегося исправлением.
// Установите параметр ревизии, чтобы показать более подробную информацию о каждой ревизии во всплывающей подсказке на правом поле страницы.
doc.LayoutOptions.RevisionOptions.ShowInBalloons = ShowInBalloons.FormatAndDelete;
doc.Save(ArtifactsDir + "Revision.ShowRevisionBalloons.pdf");
```

Показывает, как изменить внешний вид редакций.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Получить объект RevisionOptions, управляющий внешним видом ревизий.
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// Отображение ревизий вставки зеленым цветом и курсивом.
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// Отображение удаленных ревизий красным и полужирным шрифтом.
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// Один и тот же текст появится дважды в ревизии движения:
// один раз в пункте отправления и один раз в пункте прибытия.
// Визуализируем текст перемещенной версии желтым цветом с двойным перечеркиванием
// и дважды подчеркнутый синим цветом ревизию, к которой был перемещен.
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// Редактирование формата темно-красным и полужирным шрифтом.
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// Поместите толстую темно-синюю полосу в левой части страницы рядом со строками, затронутыми изменениями.
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// Показать метки исправления и исходный текст.
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// Получить перемещение, удаление, исправления форматирования и комментарии для отображения в зеленых выносках
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


