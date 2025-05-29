---
title: ListFormat.ApplyBulletDefault
linktitle: ApplyBulletDefault
articleTitle: ApplyBulletDefault
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод ApplyBulletDefault, чтобы легко создавать стильные маркированные списки в документах, повышая их читабельность и организованность.
type: docs
weight: 50
url: /ru/net/aspose.words.lists/listformat/applybulletdefault/
---
## ListFormat.ApplyBulletDefault method

Начинает новый маркированный список по умолчанию и применяет его к абзацу.

```csharp
public void ApplyBulletDefault()
```

## Примечания

Это сокращенный метод, который создает новый список с использованием шаблона bulleted по умолчанию, применяет его к абзацу и выбирает 1-й уровень списка.

## Примеры

Показывает, как создавать маркированные и нумерованные списки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Список позволяет нам организовывать и украшать наборы абзацев с помощью префиксных символов и отступов.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом в списке.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 — Маркированный список:
// В этом списке перед каждым абзацем будет применен отступ и символ маркера ("•").
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Завершить маркированный список.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.ApplyNumberDefault();

// Этот абзац является первым элементом. Первый элемент нумерованного списка будет иметь "1." в качестве символа элемента списка.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Вызываем метод "ListIndent" для увеличения текущего уровня списка,
// который начнет новый автономный список с более глубоким отступом с текущего элемента первого уровня списка.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Это первые три элемента списка второго уровня, которые будут вести подсчет
// независимо от количества первого уровня списка. Согласно текущему формату списка,
// они будут иметь символы «a.», «b.» и «c.».
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Вызываем метод «ListOutdent» для возврата на предыдущий уровень списка.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Эти два абзаца продолжат отсчет первого уровня списка.
// Эти элементы будут иметь символы «2.» и «3.»
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Если мы увеличим уровень списка до уровня, на который мы ранее добавляли элементы,
 // вложенный список будет отделен от предыдущего, и его нумерация начнется с начала.
// Эти элементы списка будут иметь символы «a.», «b.», «c.», «d.» и «e».
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Снова увеличиваем отступ списка.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Завершить нумерованный список.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Смотрите также

* class [ListFormat](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
