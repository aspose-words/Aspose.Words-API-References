---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words для .NET
description: Aspose.Words.Lists.ListFormat сорт. Позволяет контролировать какое форматирование списка применяется к абзацу на С#.
type: docs
weight: 3480
url: /ru/net/aspose.words.lists/listformat/
---
## ListFormat class

Позволяет контролировать, какое форматирование списка применяется к абзацу.

Чтобы узнать больше, посетите[Работа со списками](https://docs.aspose.com/words/net/working-with-lists/) статья документации.

```csharp
public class ListFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Истинно, если к абзацу применено маркированное или нумерованное форматирование. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Получает или задает список, членом которого является этот абзац. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Возвращает форматирование уровня списка плюс любые переопределения форматирования, примененные к текущему абзацу. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Получает или задает номер уровня списка (от 0 до 8) для абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Запускает новый маркированный список по умолчанию и применяет его к абзацу. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Запускает новый нумерованный список по умолчанию и применяет его к абзацу. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Увеличивает уровень списка текущего абзаца на один уровень. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Уменьшает уровень списка текущего абзаца на один уровень. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Удаляет номера или маркеры из текущего абзаца и устанавливает нулевой уровень списка. |

## Примечания

Абзац в документе Microsoft Word может быть маркирован или пронумерован. Когда абзац маркирован или пронумерован, говорят, что к абзацу применяется форматирование списка .

Вы не создаете объекты`ListFormat` класс напрямую. Вы получаете доступ`ListFormat` как свойство другого объекта, с которым can связано форматирование списка. На данный момент объекты, которые can имеют форматирование списка:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) и[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` из[`Paragraph`](../../aspose.words/paragraph/) указывает , какое форматирование списка и уровень списка применяются к этому конкретному абзацу.

`ListFormat` из[`Style`](../../aspose.words/style/) (applicable только для стилей абзацев) позволяет указать, какое форматирование списка и уровень списка level применяются ко всем абзацам этого конкретного стиля.

`ListFormat` из[`DocumentBuilder`](../../aspose.words/documentbuilder/) обеспечивает доступ к форматированию списка в текущей позиции курсора внутри[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Само форматирование списка хранится внутри[`List`](../list/) , который хранится отдельно от абзацев. Список объектов хранится внутри[`ListCollection`](../listcollection/) коллекция. Есть один [`ListCollection`](../listcollection/) сбор за[`Document`](../../aspose.words/document/).

Абзацы физически не принадлежат списку. Абзацы just ссылаются на конкретный объект списка через[`List`](./list/) property и определенный уровень в списке через[`ListLevelNumber`](./listlevelnumber/) property. Установив эти два свойства, вы управляете тем, какие маркеры и нумерация is применяются к абзацу.

## Примеры

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и украшать наборы абзацев префиксными символами и отступами.
 // Мы можем создавать вложенные списки, увеличивая уровень отступа.
 // Мы можем начать и закончить список, используя свойство ListFormat конструктора документов.
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев путем нумерации каждого элемента.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство ListLevelNumber, мы можем повысить уровень списка
// чтобы начать автономный подсписок с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
 // На более глубоких уровнях списка используются буквы и строчные римские цифры.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// Этот список будет применять отступ и символ маркера («•») перед каждым абзацем.
// На более глубоких уровнях этого списка будут использоваться другие символы, например «■» и «○».
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Мы можем отключить форматирование списка, чтобы не форматировать последующие абзацы как списки, сняв флаг «Список».
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists/)
* сборка [Aspose.Words](../../)
