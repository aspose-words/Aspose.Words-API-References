---
title: Frameset.ChildFramesets
linktitle: ChildFramesets
articleTitle: ChildFramesets
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Frameset ChildFramesets, чтобы легко получать доступ и управлять коллекциями дочерних фреймов и страниц для улучшенного веб-дизайна.
type: docs
weight: 20
url: /ru/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Получает коллекцию дочерних фреймов и страниц фреймов.

```csharp
public FramesetCollection ChildFramesets { get; }
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

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* пространство имен [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* сборка [Aspose.Words](../../../)
