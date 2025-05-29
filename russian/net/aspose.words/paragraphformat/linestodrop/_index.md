---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat LinesToDrop увеличивает высоту буквицы в ваших документах. Оптимизируйте макет текста для получения потрясающих визуальных эффектов!
type: docs
weight: 210
url: /ru/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Возвращает или задает количество строк текста абзаца, используемых для расчета высоты буквицы.

```csharp
public int LinesToDrop { get; set; }
```

## Примеры

Показывает, как задать размер буквицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Измените свойство "LinesToDrop", чтобы обозначить абзац как буквицу,
// что превратит ее в большую заглавную букву, которая украсит следующий абзац.
// Присвойте этому свойству значение 4, чтобы задать буквице высоту четырех строк текста.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Сбросьте свойство «LinesToDrop» до 0, чтобы превратить следующий абзац в обычный абзац.
// Текст в этом абзаце будет обтекать буквицу.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
