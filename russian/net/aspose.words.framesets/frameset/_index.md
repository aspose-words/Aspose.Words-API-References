---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Framesets.Frameset для бесшовного управления фреймами в документах. Улучшите свои веб-страницы с помощью эффективной интеграции фреймов!
type: docs
weight: 3510
url: /ru/net/aspose.words.framesets/frameset/
---
## Frameset class

Представляет страницу фреймов или один фрейм на странице фреймов.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class Frameset
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Frameset](frameset/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Получает коллекцию дочерних фреймов и страниц фреймов. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Возвращает или задает URL-адрес веб-страницы или имя файла документа для отображения в этом фрейме. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Возвращает или задает значение, указывающее, является ли веб-страница или имя файла документа, указанное в the [`FrameDefaultUrl`](./framedefaulturl/) свойство — это внешний ресурс, с которым связан фрейм. |

## Примечания

Если[`ChildFramesets`](./childframesets/) свойство содержит элементы, этот экземпляр является страницей фреймов, в противном случае это один фрейм.

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

* пространство имен [Aspose.Words.Framesets](../../aspose.words.framesets/)
* сборка [Aspose.Words](../../)
