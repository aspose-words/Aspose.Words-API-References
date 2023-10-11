---
title: Field.Unlink
second_title: Справочник по API Aspose.Words для .NET
description: Field метод. Выполняет отсоединение поля.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Выполняет отсоединение поля.

```csharp
public bool Unlink()
```

### Возвращаемое значение

`истинный` если поле было несвязано, в противном случае`ЛОЖЬ` .

### Примечания

Заменяет поле самым последним результатом.

Некоторые поля, такие как поля XE (индексная запись) и поля SEQ (последовательность), невозможно отсоединить.

### Примеры

Показывает, как отменить связь поля.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../field/)
* сборка [Aspose.Words](../../../)


