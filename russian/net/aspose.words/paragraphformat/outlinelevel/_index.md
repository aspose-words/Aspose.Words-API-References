---
title: ParagraphFormat.OutlineLevel
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Определяет уровень структуры абзаца в документе.
type: docs
weight: 250
url: /ru/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Определяет уровень структуры абзаца в документе.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### Примеры

Показывает, как настроить уровни структуры абзаца для создания свертываемого текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждый абзац имеет OutlineLevel, который может быть любым числом от 1 до 9 или значением по умолчанию «BodyText».
// Присвоение свойству одного из пронумерованных значений отобразит стрелку влево
// начала абзаца.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Уровень 1 — самый верхний уровень. Если под абзацем более высокого уровня находится абзац с более низким уровнем,
// свертывание абзаца более высокого уровня приведет к сворачиванию абзаца нижнего уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Два абзаца одного уровня не схлопнутся друг с другом,
// и стрелки не сворачивают абзацы, на которые они указывают.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Значение «BodyText» по умолчанию — наименьшее, на которое может свернуть абзац любого уровня.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Смотрите также

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


