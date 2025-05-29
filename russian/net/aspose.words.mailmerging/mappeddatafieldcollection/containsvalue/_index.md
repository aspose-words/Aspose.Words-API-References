---
title: MappedDataFieldCollection.ContainsValue
linktitle: ContainsValue
articleTitle: ContainsValue
second_title: Aspose.Words для .NET
description: Узнайте, существует ли сопоставление полей в MappedDataFieldCollection с помощью метода ContainsValue. Повысьте эффективность управления данными сегодня!
type: docs
weight: 60
url: /ru/net/aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/
---
## MappedDataFieldCollection.ContainsValue method

Определяет, существует ли сопоставление из указанного поля в источнике данных в коллекции.

```csharp
public bool ContainsValue(string dataSourceFieldName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceFieldName | String | Имя поля в источнике данных чувствительно к регистру. |

### Возвращаемое значение

`истинный`если элемент найден в коллекции; в противном случае,`ЛОЖЬ`.

## Примеры

Показывает, как сопоставлять столбцы данных и поля MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния почты.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // В таблице есть столбец с именем «Column2», но нет MERGEFIELD с таким именем.
    // Также у нас есть MERGEFIELD с именем "Column3", но в источнике данных нет столбца с таким именем.
    // Если данные из "Column2" подходят для MERGEFIELD "Column3",
    // мы можем сопоставить это имя столбца с MERGEFIELD в паре ключ/значение "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Мы можем связать имя столбца источника данных с именем MERGEFIELD следующим образом.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Свяжите столбец источника данных с именем «Column2» с MERGEFIELD с именем «Column3».
    mappedDataFields.Add("Column3", "Column2");

    // Имя MERGEFIELD является «ключом» к соответствующему имени столбца источника данных «значение».
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Теперь, если мы запустим это слияние, поля MERGEFIELD "Column3" будут брать данные из "Column2" таблицы.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Мы можем перебирать элементы в этой коллекции.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Мы также можем удалять элементы из коллекции.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Создаем документ с 2 MERGEFIELD, один из которых не имеет
/// соответствующий столбец в таблице данных из метода ниже.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Создаем таблицу данных с 2 столбцами, один из которых не имеет
/// соответствующий MERGEFIELD в исходном документе из метода выше.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Смотрите также

* class [MappedDataFieldCollection](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
