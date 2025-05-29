---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words для .NET
description: Откройте для себя метод отмены связи полей, позволяющий легко отменить связь полей, улучшить управление данными и оптимизировать рабочий процесс для достижения оптимальных результатов.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

Выполняет отмену связи поля.

```csharp
public bool Unlink()
```

### Возвращаемое значение

`истинный` если поле было несвязано, в противном случае`ЛОЖЬ` .

## Примечания

Заменяет поле самым последним результатом.

Некоторые поля, такие как поля XE (запись индекса) и поля SEQ (последовательность), не могут быть отсоединены.

## Примеры

Показывает, как отменить привязку поля.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### Смотрите также

* class [Field](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
