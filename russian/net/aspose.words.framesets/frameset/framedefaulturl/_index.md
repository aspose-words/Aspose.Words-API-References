---
title: Frameset.FrameDefaultUrl
linktitle: FrameDefaultUrl
articleTitle: FrameDefaultUrl
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Frameset FrameDefaultUrl, чтобы легко задать URL-адреса веб-страниц или файлов документов для бесшовных показов кадров. Улучшите свой веб-опыт!
type: docs
weight: 30
url: /ru/net/aspose.words.framesets/frameset/framedefaulturl/
---
## Frameset.FrameDefaultUrl property

Возвращает или задает URL-адрес веб-страницы или имя файла документа для отображения в этом фрейме.

```csharp
public string FrameDefaultUrl { get; set; }
```

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

* class [Frameset](../)
* пространство имен [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* сборка [Aspose.Words](../../../)
