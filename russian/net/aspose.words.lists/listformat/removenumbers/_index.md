---
title: ListFormat.RemoveNumbers
second_title: Справочник по API Aspose.Words для .NET
description: ListFormat метод. Удаляет числа или маркеры из текущего абзаца и устанавливает нулевой уровень списка.
type: docs
weight: 90
url: /ru/net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

Удаляет числа или маркеры из текущего абзаца и устанавливает нулевой уровень списка.

```csharp
public void RemoveNumbers()
```

### Примечания

Вызов этого метода эквивалентен установке[`List`](../list/) свойство в ноль.

### Примеры

Показывает, как удалить форматирование списка из всех абзацев в основном тексте раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

Показывает, как создавать маркированные и нумерованные списки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
// Мы можем создавать вложенные списки, увеличивая уровень отступа. 
// Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Маркированный список:
// Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Конец маркированного списка.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев, нумеруя каждый элемент.
builder.ListFormat.ApplyNumberDefault();

// Этот абзац является первым элементом. Первый элемент нумерованного списка будет иметь «1». в качестве символа элемента списка.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Вызываем метод "ListIndent" для увеличения текущего уровня списка,
// который начнет новый автономный список с более глубоким отступом от текущего элемента первого уровня списка.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Это первые три элемента списка второго уровня списка, в котором будет вестись подсчет
// независимо от счетчика первого уровня списка. Согласно текущему формату списка,
// они будут иметь символы «a.», «b.» и «c.».
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Вызовите метод "ListOutdent", чтобы вернуться на предыдущий уровень списка.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Эти два абзаца продолжат отсчет первого уровня списка.
// Эти элементы будут иметь символы «2.» и «3.»
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Если мы увеличим уровень списка до уровня, на который мы добавили элементы ранее,
// вложенный список будет отделен от предыдущего, и его нумерация начнется с начала. 
// Эти элементы списка будут иметь символы «a.», «b.», «c.», «d.» и «e».
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Снова выступаем за уровень списка.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Конец нумерованного списка.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Смотрите также

* class [ListFormat](../)
* пространство имен [Aspose.Words.Lists](../../listformat/)
* сборка [Aspose.Words](../../../)


