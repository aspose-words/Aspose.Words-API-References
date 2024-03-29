---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words для .NET
description: PageSetup LineNumberRestartMode свойство. Получает или задает способ нумерации строк то есть начинается ли она заново в начале новой страницы или раздела или выполняется непрерывно на С#.
type: docs
weight: 230
url: /ru/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Получает или задает способ нумерации строк, то есть начинается ли она заново в начале новой страницы или раздела или выполняется непрерывно.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

## Примеры

Показывает, как включить нумерацию строк для раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Мы можем использовать объект PageSetup раздела для отображения чисел слева от текстовых строк раздела.
// Это то же поведение, что и объект List,
// но он охватывает весь раздел и никак не изменяет текст.
// Наш раздел будет перезапускать нумерацию на каждой новой странице с 1 и отображать номер,
// если оно кратно 3, то через 50 пт слева от строки.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Счетчик строк пропустит любой абзац с флагом «SuppressLineNumbers», установленным в «true».
// Этот абзац находится на 15-й строке, что кратно 3, и поэтому обычно отображает номер строки.
// Счетчик строк раздела также будет игнорировать эту строку, считать следующую строку 15-й,
// и продолжаем отсчет с этого момента.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Смотрите также

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
