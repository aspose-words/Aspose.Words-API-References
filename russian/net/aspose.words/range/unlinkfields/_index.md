---
title: Range.UnlinkFields
second_title: Справочник по API Aspose.Words для .NET
description: Range метод. Отменяет связь полей в этом диапазоне.
type: docs
weight: 110
url: /ru/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

Отменяет связь полей в этом диапазоне.

```csharp
public void UnlinkFields()
```

### Примечания

Заменяет все поля в этом диапазоне самыми последними результатами.

Чтобы отменить связь полей во всем документе, используйте`UnlinkFields`.

### Примеры

Показывает, как отменить связь всех полей в диапазоне.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../range/)
* сборка [Aspose.Words](../../../)


