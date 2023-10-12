---
title: ParagraphFormat.CharacterUnitLeftIndent
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает значение левого отступа в символах для указанных абзацев.
type: docs
weight: 80
url: /ru/net/aspose.words/paragraphformat/characterunitleftindent/
---
## ParagraphFormat.CharacterUnitLeftIndent property

Получает или задает значение левого отступа (в символах) для указанных абзацев.

```csharp
public double CharacterUnitLeftIndent { get; set; }
```

### Примеры

Показывает, как изменить интервал между абзацами и отступы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// Ниже приведены пять различных вариантов интервалов, а также свойства, на которые косвенно влияет их конфигурация.
// 1 - Отступ слева:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Отступ справа:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Висячий отступ:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Межстрочный интервал перед абзацами:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Межстрочный интервал после абзацев:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


