---
title: FieldMergingArgsBase.TableName
linktitle: TableName
articleTitle: TableName
second_title: Aspose.Words для .NET
description: FieldMergingArgsBase TableName свойство. Получает имя таблицы данных для текущей операции слияния или пустую строку если имя недоступно на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.mailmerging/fieldmergingargsbase/tablename/
---
## FieldMergingArgsBase.TableName property

Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно.

```csharp
public string TableName { get; }
```

## Примеры

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

* class [FieldMergingArgsBase](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
