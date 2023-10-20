---
title: ListFormat.ApplyNumberDefault
linktitle: ApplyNumberDefault
articleTitle: ApplyNumberDefault
second_title: Aspose.Words для .NET
description: ListFormat ApplyNumberDefault метод. Запускает новый нумерованный список по умолчанию и применяет его к абзацу на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.lists/listformat/applynumberdefault/
---
## ListFormat.ApplyNumberDefault method

Запускает новый нумерованный список по умолчанию и применяет его к абзацу.

```csharp
public void ApplyNumberDefault()
```

## Примечания

Это сокращенный метод, который создает новый список с использованием шаблона Numbered по умолчанию, применяет его к абзацу и выбирает первый уровень списка.

## Примеры

Показывает, как создавать маркированные и нумерованные списки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Маркированный список:
// Этот список будет применять отступ и символ маркера («•») перед каждым абзацем.
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

// Этот абзац является первым элементом. Первый элемент нумерованного списка будет иметь цифру «1». в качестве символа элемента списка.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Вызов метода ListIndent для увеличения текущего уровня списка,
// который начнет новый автономный список с более глубоким отступом от текущего элемента первого уровня списка.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Это первые три элемента списка второго уровня списка, которые будут поддерживать счетчик
// независимо от счетчика первого уровня списка. Согласно текущему формату списка,
// они будут иметь символы «a.», «b.» и «c.».
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Вызов метода ListOutdent для возврата на предыдущий уровень списка.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Эти два абзаца продолжат отсчет первого уровня списка.
// Эти элементы будут иметь символы «2.» и «3».
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Если мы увеличим уровень списка до уровня, на который мы ранее добавляли элементы,
 // вложенный список будет отдельным от предыдущего, и его нумерация начнется с начала.
// Эти элементы списка будут иметь символы «a.», «b.», «c.», «d.» и «e».
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Снова повышаем уровень списка.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Завершаем нумерованный список.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Смотрите также

* class [ListFormat](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
