---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldAutoNum SeparatorCharacter, легко настройте свой символ-разделитель для улучшенного форматирования данных и повышения удобства использования.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Возвращает или задает символ разделителя, который будет использоваться.

```csharp
public string SeparatorCharacter { get; set; }
```

## Примеры

Показывает, как нумеровать абзацы с помощью полей автонумерации.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждое поле AUTONUM отображает текущее значение текущего количества полей AUTONUM,
// позволяя нам автоматически нумеровать элементы, как в нумерованном списке.
// В этом поле будет отображаться число «1.».
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Символом-разделителем, который появляется в поле результата сразу после числа, по умолчанию является точка.
// Если мы оставим это свойство пустым, наше второе поле AUTONUM будет отображать «2.» в документе.
Assert.IsNull(field.SeparatorCharacter);

// Мы можем установить это свойство для применения первого символа его строки в качестве нового символа-разделителя.
// В этом случае наше поле AUTONUM теперь будет отображать «2:».
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Смотрите также

* class [FieldAutoNum](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
