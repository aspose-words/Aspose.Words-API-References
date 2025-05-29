---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat WidowControl обеспечивает расположение первой и последней строк текста на одной странице для лучшей читаемости.
type: docs
weight: 410
url: /ru/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

True, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца.

```csharp
public bool WidowControl { get; set; }
```

## Примеры

Показывает, как включить контроль вдов/сирот для абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Когда мы пишем текст, который не помещается на одной странице, одна строка может перекинуться на следующую страницу.
// Единственная строка, которая оказывается на следующей странице, называется «сиротой»,
// а предыдущая строка, где сирота обрывалась, называется «Вдова».
// Мы можем исправить сирот и вдов, изменив текст с помощью размера шрифта, интервала или полей страницы.
// Если мы хотим сохранить размеры нашего документа, мы можем установить этот флаг в значение «true»
// чтобы поставить вдов на одну ступень с их сиротами.
// Если оставить этот флаг как «false», в тексте останутся пары «вдова/сирота».
// Каждый абзац имеет эту настройку, доступную в Microsoft Word через Главная -> Абзац -> Параметры абзаца
// (кнопка в правом нижнем углу вкладки «Абзац») -> «Управление вдовами/сиротами».
builder.ParagraphFormat.WidowControl = widowControl; 

// Вставьте текст, который создает сироту и вдову.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
