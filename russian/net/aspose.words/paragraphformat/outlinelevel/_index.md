---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat OutlineLevel, которое позволит легко определить иерархию абзацев в документах, улучшить организацию и читабельность.
type: docs
weight: 260
url: /ru/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Указывает уровень структуры абзаца в документе.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## Примеры

Показывает, как настроить уровни структуры абзаца для создания сворачиваемого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац имеет OutlineLevel, который может быть любым числом от 1 до 9 или иметь значение по умолчанию «BodyText».
// Установка свойства в одно из пронумерованных значений отобразит стрелку влево
// начала абзаца.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Уровень 1 — самый верхний уровень. Если есть абзац с более низким уровнем под абзацем с более высоким уровнем,
// сворачивание абзаца более высокого уровня приведет к сворачиванию абзаца более низкого уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Два абзаца одного уровня не будут сворачивать друг друга,
// и стрелки не сворачивают абзацы, на которые они указывают.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Значение "BodyText" по умолчанию — наименьшее, при котором абзац любого уровня может свернуться.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Смотрите также

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
