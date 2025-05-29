---
title: Document.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words для .NET
description: Узнайте, как использовать метод UnlinkFields для эффективного удаления связей полей во всем документе, что улучшит процесс редактирования.
type: docs
weight: 780
url: /ru/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Отменяет связь полей во всем документе.

```csharp
public void UnlinkFields()
```

## Примечания

Заменяет все поля во всем документе самыми последними результатами.

Чтобы отменить связь полей в определенной части документа, используйте[`UnlinkFields`](../../range/unlinkfields/).

## Примеры

Показывает, как отменить связь всех полей в документе.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
