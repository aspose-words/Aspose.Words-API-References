---
title: DocumentBuilder.MoveToMergeField
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Перемещает курсор в позицию сразу за указанным полем слияния и удаляет поле слияния.
type: docs
weight: 560
url: /ru/net/aspose.words/documentbuilder/movetomergefield/
---
## MoveToMergeField(string) {#movetomergefield}

Перемещает курсор в позицию сразу за указанным полем слияния и удаляет поле слияния.

```csharp
public bool MoveToMergeField(string fieldName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | String | Нечувствительное к регистру имя поля слияния почты. |

### Возвращаемое значение

`истинный` если поле слияния было найдено и курсор был перемещен;`ЛОЖЬ` в противном случае.

### Примечания

Обратите внимание, что этот метод удаляет поле слияния из документа после перемещения курсора.

### Примеры

Показывает, как заполнить поля MERGEFIELD данными с помощью построителя документов вместо слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем несколько MERGEFIELDS, которые принимают данные из одноименных столбцов в источнике данных во время слияния почты,
// а затем заполняем их вручную.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

Показывает, как вставлять поля формы флажка в поля MERGEFIELD в качестве данных слияния во время слияния почты.

```csharp
public void InsertCheckBox()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Используйте поля MERGEFIELD с тегами "TableStart"/"TableEnd" для определения региона слияния почты.
    // который принадлежит источнику данных с именем «StudentCourse» и имеет поле MERGEFIELD, которое принимает данные из столбца с именем «CourseName».
    builder.StartTable();
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableStart:StudentCourse ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  CourseName ");
    builder.InsertCell();
    builder.InsertField(" MERGEFIELD  TableEnd:StudentCourse ");
    builder.EndTable();

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertCheckBox();

    DataTable dataTable = GetStudentCourseDataTable();

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMergeEvent.InsertCheckBox.docx");
}

/// <summary>
/// При обнаружении MERGEFIELD с определенным именем вставляет поле формы флажка вместо текста данных слияния.
/// </summary>
private class HandleMergeFieldInsertCheckBox : IFieldMergingCallback
{
    /// <summary>
    /// Вызывается, когда слияние почты объединяет данные в MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName == "CourseName")
        {
            Assert.AreEqual("StudentCourse", args.TableName);

            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.FieldName);
            builder.InsertCheckBox(args.DocumentFieldName + mCheckBoxCount, false, 0);

            string fieldValue = args.FieldValue.ToString();

            // В этом случае для каждого индекса записи «n» соответствующее значение поля — «Курс n».
            Assert.AreEqual(char.GetNumericValue(fieldValue[7]), args.RecordIndex);

            builder.Write(fieldValue);
            mCheckBoxCount++;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Ничего не делать.
    }

    private int mCheckBoxCount;
}

/// <summary>
/// Создает источник данных слияния почты.
/// </summary>
private static DataTable GetStudentCourseDataTable()
{
    DataTable dataTable = new DataTable("StudentCourse");
    dataTable.Columns.Add("CourseName");
    for (int i = 0; i < 10; i++)
    {
        DataRow datarow = dataTable.NewRow();
        dataTable.Rows.Add(datarow);
        datarow[0] = "Course " + i;
    }

    return dataTable;
}
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)

---

## MoveToMergeField(string, bool, bool) {#movetomergefield_1}

Перемещает поле слияния в указанное поле слияния.

```csharp
public bool MoveToMergeField(string fieldName, bool isAfter, bool isDeleteField)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | String | Нечувствительное к регистру имя поля слияния почты. |
| isAfter | Boolean | Когда`истинный` , перемещает курсор после конца поля. Когда`ЛОЖЬ` , перемещает курсор до начала поля. |
| isDeleteField | Boolean | Когда`истинный`, удаляет поле слияния. |

### Возвращаемое значение

`истинный` если поле слияния было найдено и курсор был перемещен;`ЛОЖЬ` в противном случае.

### Примеры

Показывает, как вставлять поля и перемещать к ним курсор построителя документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Перемещаем курсор к первому MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Обратите внимание, что курсор размещается сразу после первого поля MERGEFIELD и перед вторым.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Если мы хотим отредактировать код или содержимое поля с помощью построителя,
// его курсор должен находиться внутри поля.
// Чтобы поместить его внутри поля, нам нужно будет вызвать метод MoveTo конструктора документов
// и передаем начало поля или узел-разделитель в качестве аргумента.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Смотрите также

* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


