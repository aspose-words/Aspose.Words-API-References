---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Document VersionsCount, чтобы легко отслеживать количество сохраненных версий документов в файлах DOC для лучшего управления и организации.
type: docs
weight: 480
url: /ru/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Возвращает количество версий документа, сохраненных в документе DOC.

```csharp
public int VersionsCount { get; }
```

## Примечания

Версии в Microsoft Word доступны через меню Файл/Версии. Microsoft Word поддерживает версии только для файлов DOC.

Это свойство позволяет определить, были ли версии документа, сохраненные в этом документе до того, как он был открыт в Aspose.Words. Aspose.Words не предоставляет другой поддержки версий документа. Если вы сохраните этот документ с помощью Aspose.Words, документ будет сохранен без версий.

## Примеры

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
