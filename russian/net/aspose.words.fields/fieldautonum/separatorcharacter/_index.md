---
title: FieldAutoNum.SeparatorCharacter
second_title: Справочник по API Aspose.Words для .NET
description: FieldAutoNum свойство. Получает или задает используемый символразделитель.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Получает или задает используемый символ-разделитель.

```csharp
public string SeparatorCharacter { get; set; }
```

### Примеры

Показывает, как нумеровать абзацы с помощью полей autonum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Каждое поле AUTONUM отображает текущее значение счетчика полей AUTONUM,
// что позволяет нам автоматически нумеровать элементы, как в нумерованном списке.
// В этом поле будет отображаться число «1.».
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Знак-разделитель, который появляется в поле результата сразу после числа, по умолчанию является точкой.
// Если мы оставим это свойство пустым, наше второе поле AUTONUM будет отображать «2». в документе.
Assert.IsNull(field.SeparatorCharacter);

// Мы можем установить это свойство, чтобы применить первый символ его строки в качестве нового символа-разделителя.
// В этом случае в нашем поле AUTONUM теперь будет отображаться "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Смотрите также

* class [FieldAutoNum](../)
* пространство имен [Aspose.Words.Fields](../../fieldautonum/)
* сборка [Aspose.Words](../../../)


