---
title: Document.Compliance
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает версию соответствия OOXML определенную на основе содержимого загруженного документа. Имеет смысл только для документов OOXML.
type: docs
weight: 60
url: /ru/net/aspose.words/document/compliance/
---
## Document.Compliance property

Получает версию соответствия OOXML, определенную на основе содержимого загруженного документа. Имеет смысл только для документов OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

### Примечания

Если вы создали новый пустой документ или загрузили документ, отличный от OOXML, document возвращаетEcma376_2006 ценить.

### Примеры

Показывает, как прочитать версию загруженного документа, соответствующую требованиям Open Office XML.

```csharp
// Версия соответствия различается для документов, созданных в разных версиях Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Смотрите также

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


