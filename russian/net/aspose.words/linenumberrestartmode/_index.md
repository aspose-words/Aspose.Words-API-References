---
title: Enum LineNumberRestartMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.LineNumberRestartMode перечисление. Определяет когда перезапускается автоматическая нумерация строк.
type: docs
weight: 3430
url: /ru/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Определяет, когда перезапускается автоматическая нумерация строк.

```csharp
public enum LineNumberRestartMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| RestartPage | `0` | Нумерация строк возобновляется в начале каждой страницы. |
| RestartSection | `1` | Нумерация строк возобновляется с начала раздела. |
| Continuous | `2` | Нумерация строк непрерывная из предыдущего раздела. |

### Примеры

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


