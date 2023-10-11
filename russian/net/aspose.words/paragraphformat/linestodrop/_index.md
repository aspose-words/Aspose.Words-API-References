---
title: ParagraphFormat.LinesToDrop
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает количество строк текста абзаца используемого для расчета высоты буквицы.
type: docs
weight: 210
url: /ru/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Получает или задает количество строк текста абзаца, используемого для расчета высоты буквицы.

```csharp
public int LinesToDrop { get; set; }
```

### Примеры

Показывает, как установить размер буквицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Измените свойство LinesToDrop, чтобы обозначить абзац как буквицу,
// что превратит его в большую заглавную букву, которая украсит следующий абзац.
// Присвойте этому свойству значение 4, чтобы буквица имела высоту в четыре текстовые строки.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Сбрасываем свойство LinesToDrop на 0, чтобы превратить следующий абзац в обычный абзац.
// Текст в этом абзаце будет обтекать буквицу.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


