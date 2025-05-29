---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Footnote ActualReferenceMark, чтобы получить доступ к точному тексту справочных знаков в ваших документах, что повышает ясность и организованность.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Получает фактический текст сноски, отображаемый в документе для этой сноски.

```csharp
public string ActualReferenceMark { get; }
```

## Примечания

Для первоначального заполнения значений этого свойства для всех контрольных меток документа или для обновления значений после изменений в документе, которые могут повлиять на контрольные метки, необходимо выполнить [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) method. Обновление полей ([`UpdateFields`](../../../aspose.words/document/updatefields/) ) также может быть необходимо для получения правильного результата.

## Примеры

Показывает, как получить реальный знак ссылки на сноску.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### Смотрите также

* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
