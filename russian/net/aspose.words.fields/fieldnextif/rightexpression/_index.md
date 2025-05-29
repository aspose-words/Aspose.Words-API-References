---
title: FieldNextIf.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldNextIf RightExpression, чтобы легко управлять и настраивать правую часть выражений сравнения для улучшенной обработки данных.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldnextif/rightexpression/
---
## FieldNextIf.RightExpression property

Возвращает или задает правую часть выражения сравнения.

```csharp
public string RightExpression { get; set; }
```

## Примеры

Показывает, как использовать поля NEXT/NEXTIF для объединения нескольких строк на одной странице во время слияния почты.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Создаем источник данных для нашего слияния с 3 строками.
    // Слияние почты, использующее эту таблицу, обычно создает трехстраничный документ.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Если у нас есть несколько полей слияния с одинаковым FieldName,
    // они будут получать данные из одной и той же строки источника данных и отображать одно и то же значение после слияния.
    // Поле NEXT сообщает слиянию немедленно переместиться на одну строку вниз,
    // что означает, что любые поля MERGEFIELD, следующие за полем NEXT, получат данные из следующей строки.
    // Никогда не пытайтесь перейти к следующей строке, если вы уже находитесь на предыдущей строке.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // После слияния значения источника данных, которые принимают эти MERGEFIELD
     // окажется на той же странице, что и MERGEFIELD выше.
    InsertMergeFields(builder, "Second row: ");

    // Поле NEXTIF имеет ту же функцию, что и поле NEXT,
    // но он переходит к следующей строке только в том случае, если утверждение, составленное на основе следующих 3 свойств, является истинным.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Если сравнение, подтвержденное указанным выше полем, верно,
    // следующие 3 поля слияния будут брать данные из третьей строки.
    // В противном случае эти поля снова возьмут данные из строки 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Наш источник данных содержит 3 строки, и мы пропустили строки дважды.
    // Наш выходной документ будет иметь 1 страницу с данными из всех 3 строк.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Использует конструктор документов для вставки полей MERGEFIELD для источника данных, содержащего столбцы с именами «Courtesy Title», «First Name» и «Last Name».
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Использует конструктор документов для вставки MERRGEFIELD с указанными свойствами.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Смотрите также

* class [FieldNextIf](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
