---
title: Document.VersionsCount
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает количество версий документа хранящихся в документе DOC.
type: docs
weight: 460
url: /ru/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Получает количество версий документа, хранящихся в документе DOC.

```csharp
public int VersionsCount { get; }
```

### Примечания

Доступ к версиям в Microsoft Word осуществляется через меню «Файл/Версии». Microsoft Word поддерживает версии только для файлов DOC.

Это свойство позволяет определить, хранились ли в этом document версии документа до того, как он был открыт в Aspose.Words. Aspose.Words не обеспечивает никакой другой поддержки версий документа. Если вы сохраните этот документ с помощью Aspose.Words, документ будет сохранен без версий.

### Примеры

Показывает, как работать с функцией подсчета версий старых документов Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Мы можем прочитать это свойство документа, но не можем сохранить его при сохранении.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


