---
title: ListFormat
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет контролировать какое форматирование списка применяется к абзацу.
type: docs
weight: 3280
url: /ru/net/aspose.words.lists/listformat/
---
## ListFormat class

Позволяет контролировать, какое форматирование списка применяется к абзацу.

```csharp
public class ListFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem) { get; } | Истинно, если к абзацу применено маркированное или нумерованное форматирование. |
| [List](../../aspose.words.lists/listformat/list) { get; set; } | Получает или задает список, членом которого является этот абзац. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel) { get; } | Возвращает форматирование на уровне списка плюс любые изменения форматирования, примененные к текущему абзацу. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber) { get; set; } | Получает или задает номер уровня списка (от 0 до 8) для абзаца. |

## Методы

| Имя | Описание |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault)() | Запускает новый маркированный список по умолчанию и применяет его к абзацу. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault)() | Запускает новый нумерованный список по умолчанию и применяет его к абзацу. |
| [ListIndent](../../aspose.words.lists/listformat/listindent)() | Увеличивает уровень списка текущего абзаца на один уровень. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent)() | Уменьшает уровень списка текущего абзаца на один уровень. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers)() | Удаляет числа или маркеры из текущего абзаца и устанавливает нулевой уровень списка. |

### Примечания

Абзац в документе Microsoft Word может быть промаркирован или пронумерован. Когда абзац промаркирован или пронумерован, говорят, что форматирование списка применяется к абзацу.

Вы не создаете объекты[`ListFormat`](../listformat) класс напрямую. Вы получаете доступ[`ListFormat`](../listformat) как свойство другого объекта, который может иметь связанное с ним форматирование списка. На данный момент объекты, которые can имеют форматирование списка:[`Paragraph`](../../aspose.words/paragraph) , [`Style`](../../aspose.words/style) а также[`DocumentBuilder`](../../aspose.words/documentbuilder).

[`ListFormat`](../listformat) из[`Paragraph`](../../aspose.words/paragraph) указывает , какое форматирование списка и уровень списка применяются к этому конкретному абзацу.

[`ListFormat`](../listformat) из[`Style`](../../aspose.words/style)(применимо только к стилям абзаца) позволяет указать, какое форматирование списка и уровень списка применяются ко всем абзацам этого конкретного стиля.

[`ListFormat`](../listformat) из[`DocumentBuilder`](../../aspose.words/documentbuilder) обеспечивает доступ к форматированию списка в текущей позиции курсора внутри[`DocumentBuilder`](../../aspose.words/documentbuilder).

Само форматирование списка хранится внутри[`List`](../list) объект, который хранится отдельно от абзацев. Список objects хранится внутри[`ListCollection`](../listcollection) коллекция. Есть сингл [`ListCollection`](../listcollection) сбор за[`Document`](../../aspose.words/document).

Абзацы физически не принадлежат списку. Параграфы just ссылаются на конкретный объект списка через[`List`](./list) property и определенный уровень в списке через[`ListLevelNumber`](./listlevelnumber) property. Установив эти два свойства, вы определяете, какие маркеры и нумерация is применяются к абзацу.

### Примеры

Показывает, как работать с уровнями списка.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Список позволяет нам организовывать и оформлять наборы абзацев префиксными символами и отступами.
// Мы можем создавать вложенные списки, увеличивая уровень отступа. 
// Мы можем начать и закончить список, используя свойство "ListFormat" конструктора документов. 
// Каждый абзац, который мы добавляем между началом и концом списка, станет элементом списка.
// Ниже приведены два типа списков, которые мы можем создать с помощью конструктора документов.
// 1 - Нумерованный список:
// Нумерованные списки создают логический порядок абзацев, нумеруя каждый элемент.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Установив свойство "ListLevelNumber", мы можем увеличить уровень списка
// чтобы начать автономный подсписок с текущего элемента списка.
// Шаблон списка Microsoft Word под названием «NumberDefault» использует числа для создания уровней списка для первого уровня списка.
// Более глубокие уровни списка используют буквы и строчные римские цифры. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Маркированный список:
// Этот список будет применять отступ и символ маркера ("•") перед каждым абзацем.
// На более глубоких уровнях этого списка будут использоваться другие символы, такие как "■" и "○".
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

* пространство имен [Aspose.Words.Lists](../../aspose.words.lists)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
