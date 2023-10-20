---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words для .NET
description: ParagraphFormat WidowControl свойство. Истинно если первая и последняя строки абзаца должны оставаться на той же странице что и остальная часть абзаца на С#.
type: docs
weight: 400
url: /ru/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Истинно, если первая и последняя строки абзаца должны оставаться на той же странице, что и остальная часть абзаца.

```csharp
public bool WidowControl { get; set; }
```

## Примеры

Показывает, как включить управление «висящим» или «сиротским» абзацем.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Когда мы пишем текст, который не умещается на одной странице, одна строка может перекинуться на следующую страницу.
// Единственная строка, которая попадает на следующую страницу, называется «Сирота»,
// и предыдущая строка, где обрывался сирота, называется «Вдова».
// Мы можем исправить «сирот» и «вдовевшие» элементы, изменив порядок текста с помощью размера шрифта, интервалов или полей страницы.
// Если мы хотим сохранить размеры нашего документа, мы можем установить для этого флага значение «истина»
 // чтобы поместить вдов на ту же страницу, что и их сирот.
// Если оставить этот флаг равным «false», в тексте останутся пары вдовец/сирота.
// Каждый абзац имеет эту настройку, доступную в Microsoft Word через главную страницу -> gt; Абзац -> Настройки абзаца
// (кнопка в правом нижнем углу вкладки «Абзац») -> -> «Контроль вдовы/сироты».
builder.ParagraphFormat.WidowControl = widowControl; 

// Вставляем текст, который создает сироту и вдову.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
