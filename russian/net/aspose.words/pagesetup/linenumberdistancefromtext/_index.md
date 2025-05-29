---
title: PageSetup.LineNumberDistanceFromText
linktitle: LineNumberDistanceFromText
articleTitle: LineNumberDistanceFromText
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup LineNumberDistanceFromText, которое позволяет легко настроить интервал между номерами строк и текстом документа для улучшения его читаемости.
type: docs
weight: 220
url: /ru/net/aspose.words/pagesetup/linenumberdistancefromtext/
---
## PageSetup.LineNumberDistanceFromText property

Возвращает или задает расстояние между правым краем номеров строк и левым краем документа.

```csharp
public double LineNumberDistanceFromText { get; set; }
```

## Примечания

Установите это свойство на ноль для автоматического расстояния между номерами строк и текстом документа.

## Примеры

Показывает, как включить нумерацию строк для раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем использовать объект PageSetup раздела для отображения чисел слева от текстовых строк раздела.
// Это то же самое поведение, что и у объекта List,
// но он охватывает весь раздел и никак не изменяет текст.
// Наш раздел будет перезапускать нумерацию на каждой новой странице с 1 и отображать номер,
// если кратно 3, на расстоянии 50 пунктов слева от строки.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Счетчик строк пропустит любой абзац, у которого флаг «SuppressLineNumbers» установлен в значение «true».
// Этот абзац находится на 15-й строке, что кратно 3, и поэтому обычно отображает номер строки.
// Счетчик строк раздела также проигнорирует эту строку, считая следующую строку 15-й,
// и продолжаем отсчет с этой точки.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
