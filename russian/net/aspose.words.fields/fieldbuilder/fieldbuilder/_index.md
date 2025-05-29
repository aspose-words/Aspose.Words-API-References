---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words для .NET
description: Откройте для себя FieldBuilder, мощный инструмент для легкого создания и управления полями в ваших проектах. Оптимизируйте свой рабочий процесс сегодня!
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
| fieldType | FieldType | Тип поля для строительства. |

## Примеры

Показывает, как создать и вставить поле с помощью конструктора полей.

```csharp
Document doc = new Document();

// Удобный способ добавления текстового содержимого в документ — использование конструктора документов.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// У полей есть свой конструктор, который мы можем использовать для построения кода поля по частям.
// В этом случае мы создадим поле BARCODE, представляющее почтовый индекс США,
// а затем вставьте его перед Run.
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
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
