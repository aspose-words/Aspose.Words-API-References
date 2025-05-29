---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Frameset для документов. Получите экземпляр Frameset для бесшовной интеграции страниц с фреймами. Улучшите свой веб-опыт сегодня!
type: docs
weight: 170
url: /ru/net/aspose.words/document/frameset/
---
## Document.Frameset property

Возвращает`Frameset` пример, если этот документ представляет собой страницу фреймов.

```csharp
public Frameset Frameset { get; }
```

## Примечания

Если документ не оформлен, свойство имеет`нулевой` значение.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
