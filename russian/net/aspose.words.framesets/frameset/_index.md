---
title: Class Frameset
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Framesets.Frameset сорт. Представляет страницу кадров или отдельный кадр на странице кадров.
type: docs
weight: 3080
url: /ru/net/aspose.words.framesets/frameset/
---
## Frameset class

Представляет страницу кадров или отдельный кадр на странице кадров.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

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
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Получает или задает URL-адрес веб-страницы или имя файла документа для отображения в этом фрейме. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Получает или задает значение, указывающее, указано ли имя веб-страницы или файла документа, указанное в the .[`FrameDefaultUrl`](./framedefaulturl/) свойство — это внешний ресурс, с которым связан фрейм. |

### Примечания

Если[`ChildFramesets`](./childframesets/) Свойство содержит элементы, этот экземпляр является страницей кадров, в противном случае это один кадр.

### Примеры

Показывает, как получить доступ к фреймам на странице.

```csharp
// Документ содержит несколько фреймов со ссылками на другие документы.
Document doc = new Document(MyDir + "Frameset.docx");

// Мы можем проверить URL-адрес по умолчанию (URL-адрес веб-страницы или локального документа) или является ли фрейм внешним ресурсом.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Изменяем свойства одного из наших фреймов.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Смотрите также

* пространство имен [Aspose.Words.Framesets](../../aspose.words.framesets/)
* сборка [Aspose.Words](../../)


