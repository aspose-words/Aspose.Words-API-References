---
title: Frameset.IsFrameLinkToFile
second_title: Справочник по API Aspose.Words для .NET
description: Frameset свойство. Получает или задает значение указывающее указано ли имя вебстраницы или файла документа указанное в the .FrameDefaultUrl свойство  это внешний ресурс с которым связан фрейм.
type: docs
weight: 40
url: /ru/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Получает или задает значение, указывающее, указано ли имя веб-страницы или файла документа, указанное в the .[`FrameDefaultUrl`](../framedefaulturl/) свойство — это внешний ресурс, с которым связан фрейм.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

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

* class [Frameset](../)
* пространство имен [Aspose.Words.Framesets](../../frameset/)
* сборка [Aspose.Words](../../../)


