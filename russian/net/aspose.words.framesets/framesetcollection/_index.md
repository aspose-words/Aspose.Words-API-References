---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words FramesetCollection — ваше универсальное решение для легкого управления несколькими экземплярами Frameset при обработке документов.
type: docs
weight: 3520
url: /ru/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Представляет коллекцию экземпляров[`Frameset`](../frameset/) класс.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Возвращает количество кадров или страниц кадров, содержащихся в коллекции. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Получает фрейм или страницу фреймов по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Возвращает перечислитель, который выполняет итерацию по коллекции. |

## Примеры

Показывает, как получить доступ к фреймам на странице.

```csharp
// Документ содержит несколько фреймов со ссылками на другие документы.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Мы можем проверить URL-адрес по умолчанию (URL-адрес веб-страницы или локального документа) или является ли фрейм внешним ресурсом.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Изменим свойства одного из наших кадров.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Смотрите также

* class [Frameset](../frameset/)
* пространство имен [Aspose.Words.Framesets](../../aspose.words.framesets/)
* сборка [Aspose.Words](../../)
