---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words для .NET
description: FieldAutoNum SeparatorCharacter свойство. Получает или задает используемый символразделитель на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Получает или задает используемый символ-разделитель.

```csharp
public string SeparatorCharacter { get; set; }
```

## Примеры

Показывает, как нумеровать абзацы с помощью полей автонумерации.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// В каждом поле AUTONUM отображается текущее значение счетчика полей AUTONUM,
// что позволяет нам автоматически нумеровать элементы, как в нумерованном списке.
// В этом поле будет отображаться число «1».
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Символ-разделитель, который появляется в результате поля сразу после числа, по умолчанию является точкой.
// Если мы оставим это свойство нулевым, наше второе поле AUTONUM отобразит «2». в документе.
Assert.IsNull(field.SeparatorCharacter);

// Мы можем установить это свойство, чтобы применить первый символ строки в качестве нового символа-разделителя.
// В этом случае наше поле AUTONUM теперь будет отображать «2:».
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Смотрите также

* class [FieldAutoNum](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
