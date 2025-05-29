---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.TabStop, ваше решение для пользовательских табуляций в форматировании документов. Улучшите свои документы с точностью и легкостью!
type: docs
weight: 7050
url: /ru/net/aspose.words/tabstop/
---
## TabStop class

Представляет собой одну пользовательскую позицию табуляции.`TabStop` объект является членом the [`TabStopCollection`](../tabstopcollection/) коллекция.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public sealed class TabStop
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | Инициализирует новый экземпляр этого класса. |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Возвращает или задает выравнивание текста на этой позиции табуляции. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Возврат`истинный` если эта позиция табуляции очищает все существующие позиции табуляции в этой позиции. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Возвращает или задает тип линии выноски, отображаемой под символом табуляции. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Получает позицию табуляции в пунктах. |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | Сравнивает с указанным`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Вычисляет хэш-код для этого объекта. |

## Примечания

Обычно табуляция указывает позицию, в которой существует табуляция. Но поскольку табуляции могут быть унаследованы от родительских стилей, может потребоваться, чтобы дочерний объект явно определял, что в данной позиции нет табуляции. Чтобы очистить унаследованную табуляцию в данной позиции, создайте`TabStop` объект и set [`Alignment`](./alignment/) кClear.

Для получения более подробной информации см.[`TabStopCollection`](../tabstopcollection/).

## Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с оглавлением.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Пройти по всем абзацам со стилями, основанными на результате TOC; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получаем первую табуляцию, используемую в этом абзаце. Это должна быть табуляция, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Заменить первую остановку табуляции по умолчанию на пользовательскую остановку табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
