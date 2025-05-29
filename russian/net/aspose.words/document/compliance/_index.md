---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words для .NET
description: Обеспечьте соответствие ваших документов OOXML стандартам без особых усилий. Наш инструмент анализирует содержимое для проверки соответствия OOXML, повышая целостность документа.
type: docs
weight: 70
url: /ru/net/aspose.words/document/compliance/
---
## Document.Compliance property

Получает версию соответствия OOXML, определенную из загруженного содержимого документа. Имеет смысл только для документов OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Примечания

Если вы создали новый пустой документ или загрузили не OOXML document возвращаетEcma376_2006 ценить.

## Примеры

Показывает, как прочитать версию соответствия Open Office XML загруженного документа.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
