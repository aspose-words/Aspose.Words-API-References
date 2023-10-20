---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words для .NET
description: Field Unlink метод. Выполняет отсоединение поля на С#.
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

## Примечания

Заменяет поле самым последним результатом.

Некоторые поля, такие как поля XE (индексная запись) и поля SEQ (последовательность), невозможно отсоединить.

## Примеры

Показывает, как отменить связь поля.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
