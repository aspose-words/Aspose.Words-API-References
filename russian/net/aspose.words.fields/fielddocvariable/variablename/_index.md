---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldDocVariable VariableName для простого управления переменными документа. Упростите поиск и улучшите управление документами сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Возвращает или задает имя переменной документа для извлечения.

```csharp
public string VariableName { get; set; }
```

## Примеры

Показывает, как использовать поля DOCPROPERTY для отображения свойств и переменных документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа использования полей DOCPROPERTY.
// 1 — Отображение встроенного свойства:
// Задайте пользовательское значение для встроенного свойства «Категория», затем вставьте поле DOCPROPERTY, которое ссылается на него.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 — Отображение пользовательской переменной документа:
// Определите пользовательскую переменную, затем сошлитесь на эту переменную с помощью поля DOCPROPERTY.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Смотрите также

* class [FieldDocVariable](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
