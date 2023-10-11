---
title: FieldBuilder.FieldBuilder
second_title: Справочник по API Aspose.Words для .NET
description: FieldBuilder строитель. Инициализирует экземплярFieldBuilder класс.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Инициализирует экземпляр[`FieldBuilder`](../) класс.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип поля для построения. |

### Примеры

Показывает, как создать и вставить поле с помощью построителя полей.

```csharp
Document doc = new Document();

// Удобный способ добавления текстового содержимого в документ — использование конструктора документов.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// У полей есть свой конструктор, который мы можем использовать для построения кода поля по частям.
// В этом случае мы создадим поле BARCODE, представляющее почтовый индекс США,
// и затем вставляем его перед Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Смотрите также

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* пространство имен [Aspose.Words.Fields](../../fieldbuilder/)
* сборка [Aspose.Words](../../../)


