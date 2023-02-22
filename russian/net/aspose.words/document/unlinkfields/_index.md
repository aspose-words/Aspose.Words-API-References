---
title: Document.UnlinkFields
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Разъединяет поля во всем документе.
type: docs
weight: 710
url: /ru/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

Разъединяет поля во всем документе.

```csharp
public void UnlinkFields()
```

### Примечания

Заменяет все поля во всем документе их самыми последними результатами.

Чтобы отменить связь полей в определенной части документа, используйте[`UnlinkFields`](../../range/unlinkfields/).

### Примеры

Показывает, как отменить связь всех полей в документе.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


