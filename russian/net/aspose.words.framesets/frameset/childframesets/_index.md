---
title: Frameset.ChildFramesets
second_title: Справочник по API Aspose.Words для .NET
description: Frameset свойство. Получает коллекцию дочерних фреймов и страниц фреймов.
type: docs
weight: 20
url: /ru/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Получает коллекцию дочерних фреймов и страниц фреймов.

```csharp
public FramesetCollection ChildFramesets { get; }
```

### Примеры

Показывает, как получить доступ к фреймам на странице.

```csharp
// Документ содержит несколько фреймов со ссылками на другие документы.
Document doc = new Document(MyDir + "Frameset.docx");

// Мы можем проверить URL-адрес по умолчанию (URL-адрес веб-страницы или локальный документ) или является ли фрейм внешним ресурсом.
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

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* пространство имен [Aspose.Words.Framesets](../../frameset/)
* сборка [Aspose.Words](../../../)


