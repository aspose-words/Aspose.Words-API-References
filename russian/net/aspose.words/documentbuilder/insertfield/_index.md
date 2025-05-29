---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью метода InsertField DocumentBuilder. Легко добавляйте и обновляйте поля Word для динамического контента и улучшения функциональности.
type: docs
weight: 330
url: /ru/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Вставляет поле Word в документ и при необходимости обновляет результат поля.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | FieldType | Тип поля для добавления. |
| updateField | Boolean | Указывает, следует ли немедленно обновить поле. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примечания

Этот метод вставляет поле в документ. Aspose.Words может обновлять поля большинства типов, но не всех. Подробнее см. the `InsertField` перегрузка.

## Примеры

Показывает, как вставить поле в документ с помощью FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем два поля, передавая флаг, который определяет, следует ли обновлять их по мере их вставки конструктором.
// В некоторых случаях обновление полей может быть затратным с точки зрения вычислений, и может быть хорошей идеей отложить обновление.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Нам нужно будет обновить эти поля вручную, используя методы обновления.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Вставляет поле Word в документ и обновляет результат поля.

```csharp
public Field InsertField(string fieldCode)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примечания

Этот метод вставляет поле в документ и немедленно обновляет результат поля. Aspose.Words может обновлять поля большинства типов, но не всех. Для получения более подробной информации см. the `InsertField` перегрузка.

## Примеры

Показывает, как вставить поле в документ, используя код поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Эта перегрузка метода InsertField автоматически обновляет вставленные поля.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Показывает, как вставлять поля и перемещать на них курсор конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Переместить курсор на первый MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Обратите внимание, что курсор размещается сразу после первого MERGEFIELD и перед вторым.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Если мы хотим редактировать код поля или содержимое поля с помощью конструктора,
// его курсор должен находиться внутри поля.
// Чтобы поместить его в поле, нам нужно вызвать метод MoveTo конструктора документов
// и передаем начальный или разделительный узел поля в качестве аргумента.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Вставляет поле Word в документ без обновления результата поля.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | String | Код поля для вставки (без фигурных скобок). |
| fieldValue | String | Значение поля для вставки. Пройти`нулевой` для полей, не имеющих значения. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примечания

Поля в документах Microsoft Word состоят из кода поля и результата поля. Код поля подобен формуле, а результат поля подобен значению, которое выдает формула. Код поля может также содержать переключатели полей , которые являются дополнительными инструкциями для выполнения определенного действия.

Вы можете переключаться между отображением кодов полей и результатов в документе in Microsoft Word с помощью сочетания клавиш Alt+F9. Коды полей отображаются между фигурными скобками ( { } ).

Чтобы создать поле, необходимо указать тип поля, код поля и значение поля «заполнитель». Если вы не уверены в синтаксисе конкретного кода поля, сначала создайте поле в Microsoft Word и переключитесь, чтобы увидеть его код поля.

Aspose.Words может вычислять результаты полей для большинства типов полей, но этот метод не обновляет результат поля автоматически. Поскольку результат поля не вычисляется автоматически, ожидается, что вы передадите некоторое строковое значение (или даже пустую строку), которое будет вставлено в результат поля. Это значение останется в результате поля как заполнитель, пока поле не будет обновлено. Чтобы обновить результат поля, вы можете вызвать[`Update`](../../../aspose.words.fields/field/update/) на объект поля returns вам или[`UpdateFields`](../../document/updatefields/) для обновления полей во всем документе.

## Примеры

Показывает, как настроить нумерацию страниц в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Перемещаем конструктор документа в основной заголовок первого раздела,
// который будет отображаться на каждой странице этого раздела.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Вставьте поле СТРАНИЦА, в котором будет отображаться номер текущей страницы.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Настройте раздел так, чтобы количество страниц, отображаемых в полях PAGE, начиналось с 5.
// Также настройте все поля PAGE для отображения номеров страниц с использованием заглавных римских цифр.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Создаем еще один основной заголовок для второго раздела с другим полем PAGE.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Настройте раздел так, чтобы количество страниц, отображаемых в полях PAGE, начиналось с 10.
// Также настройте все поля PAGE для отображения номеров страниц с использованием арабских цифр.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
