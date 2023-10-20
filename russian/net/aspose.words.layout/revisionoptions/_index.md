---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.RevisionOptions сорт. Позволяет контролировать обработку изменений документа в процессе макетирования на С#.
type: docs
weight: 3390
url: /ru/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

Позволяет контролировать обработку изменений документа в процессе макетирования.

Чтобы узнать больше, посетите[Преобразование в формат фиксированной страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) статья документации.

```csharp
public class RevisionOptions
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | Позволяет указать цвет комментариев. Значение по умолчанию:Red . |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для удаленного содержимого.Deletion . Значение по умолчанию:ByAuthor . |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применен к удаленному содержимому.Deletion . Значение по умолчанию:StrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для вставленного контента.Insertion . Значение по умолчанию:ByAuthor . |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к вставленному содержимому.Insertion . Значение по умолчанию:Underline . |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | Позволяет указать единицы измерения для комментариев к редакции. Значение по умолчанию:Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, из которых содержимое было перемещено.Moving . Значение по умолчанию:ByAuthor . |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к областям, из которых содержимое было перемещено.Moving . Значение по умолчанию:DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для областей, куда был перемещен контент.Moving . Значение по умолчанию:ByAuthor . |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | Позволяет указать эффект, который будет применяться к областям, куда был перемещен контент.Moving . Значение по умолчанию:DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для контента с изменениями свойств форматирования.FormatChange Значение по умолчанию:NoHighlight . |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | Позволяет указать эффект для областей контента при изменении свойств форматирования.FormatChange Значение по умолчанию:None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | Позволяет указать цвет, который будет использоваться для боковых полос, которые идентифицируют строки документа, содержащие измененную информацию. Значение по умолчанию:Red . |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | Получает или задает положение рендеринга полос редакций. Значение по умолчанию:Outside . |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | Получает или задает ширину ревизионных полос в точках. |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | Позволяет указать, отображаются ли изменения в выносках. Значение по умолчанию:None . |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | Позволяет указать, должен ли отображаться исходный текст вместо измененного. Значение по умолчанию:`ЛОЖЬ` . |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | Позволяет указать, должны ли полосы изменений отображаться рядом со строками, содержащими измененный контент. Значение по умолчанию:`истинный` . |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | Позволяет указать, следует ли помечать текст редакции специальной разметкой форматирования. Значение по умолчанию:`истинный` . |

## Примеры

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
