---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words для .NET
description: Откройте для себя метод Range UnlinkFields, позволяющий легко отменять связь полей в диапазоне документа, улучшая рабочий процесс и управление документами.
type: docs
weight: 120
url: /ru/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Отменяет связь полей в этом диапазоне.

```csharp
public void UnlinkFields()
```

## Примечания

Заменяет все поля в этом диапазоне последними результатами.

Чтобы отменить связь полей во всем документе, используйте`UnlinkFields`.

## Примеры

Показывает, как отменить связь всех полей в диапазоне.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
