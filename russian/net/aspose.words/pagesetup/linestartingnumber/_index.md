---
title: PageSetup.LineStartingNumber
linktitle: LineStartingNumber
articleTitle: LineStartingNumber
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство PageSetup LineStartingNumber, чтобы легко настроить начальный номер строки документа для расширенного форматирования.
type: docs
weight: 250
url: /ru/net/aspose.words/pagesetup/linestartingnumber/
---
## PageSetup.LineStartingNumber property

Получает или задает номер начальной строки.

```csharp
public int LineStartingNumber { get; set; }
```

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
