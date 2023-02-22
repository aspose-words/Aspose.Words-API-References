---
title: ParagraphFormat.OutlineLevel
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Указывает уровень структуры абзаца в документе.
type: docs
weight: 240
url: /ru/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Указывает уровень структуры абзаца в документе.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### Примеры

Показывает, как настроить уровни структуры абзаца для создания сворачиваемого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// У каждого абзаца есть OutlineLevel, который может быть любым числом от 1 до 9 или значением по умолчанию "BodyText".
// Установка свойства в одно из пронумерованных значений покажет стрелку влево
// начала абзаца.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Уровень 1 — самый верхний уровень. Если есть абзац с более низким уровнем ниже абзаца с более высоким уровнем,
// свертывание абзаца более высокого уровня приведет к сворачиванию абзаца более низкого уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Два абзаца одного уровня не будут схлопываться друг с другом,
// и стрелки не сворачивают абзацы, на которые они указывают.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Значение "BodyText" по умолчанию — наименьшее, которое может свернуть абзац любого уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Смотрите также

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


