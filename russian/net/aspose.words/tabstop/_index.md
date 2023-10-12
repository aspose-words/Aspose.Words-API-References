---
title: Class TabStop
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.TabStop сорт. Представляет одну настраиваемую позицию табуляции.TabStopобъект является членом the TabStopCollection коллекция.
type: docs
weight: 6200
url: /ru/net/aspose.words/tabstop/
---
## TabStop class

Представляет одну настраиваемую позицию табуляции.`TabStop`объект является членом the [`TabStopCollection`](../tabstopcollection/) коллекция.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) статья документации.

```csharp
public sealed class TabStop
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [TabStop](tabstop/#constructor)(double) | Инициализирует новый экземпляр этого класса. |
| [TabStop](tabstop/#constructor_1)(double, TabAlignment, TabLeader) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | Получает или задает выравнивание текста на этой позиции табуляции. |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | Возвращает`истинный` если эта позиция табуляции очищает все существующие позиции табуляции в этой позиции. |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | Получает или задает тип линии выноски, отображаемой под символом табуляции. |
| [Position](../../aspose.words/tabstop/position/) { get; } | Получает позицию табуляции в пунктах. |

## Методы

| Имя | Описание |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(TabStop) | Сравнивает с указанным`TabStop` . |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | Вычисляет хеш-код для этого объекта. |

### Примечания

Обычно позиция табуляции указывает позицию, в которой существует позиция табуляции. Но поскольку позиции табуляции могут быть унаследованы от родительских стилей, дочернему объекту object может потребоваться явно определить, что в данной позиции нет позиции табуляции. Чтобы очистить унаследованную позицию табуляции в заданной позиции, создайте`TabStop` объект и set [`Alignment`](./alignment/) кClear.

Для получения дополнительной информации см.[`TabStopCollection`](../tabstopcollection/).

### Примеры

Показывает, как изменить положение правой позиции табуляции в абзацах, связанных с содержанием.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Перебираем все абзацы со стилями на основе результатов оглавления; это любой стиль между TOC и TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Получаем первую вкладку, используемую в этом абзаце. Это должна быть вкладка, используемая для выравнивания номеров страниц.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Заменяем первую табуляцию по умолчанию, остановку на пользовательскую позицию табуляции.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


