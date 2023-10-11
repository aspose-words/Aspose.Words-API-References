---
title: MappedDataFieldCollection.Add
second_title: Справочник по API Aspose.Words для .NET
description: MappedDataFieldCollection метод. Добавляет новое сопоставление полей.
type: docs
weight: 30
url: /ru/net/aspose.words.mailmerging/mappeddatafieldcollection/add/
---
## MappedDataFieldCollection.Add method

Добавляет новое сопоставление полей.

```csharp
public void Add(string documentFieldName, string dataSourceFieldName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| documentFieldName | String | Имя поля слияния почты в документе, чувствительное к регистру. |
| dataSourceFieldName | String | Имя поля в источнике данных с учетом регистра. |

### Примеры

Показывает, как сопоставить столбцы данных и поля MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния почты.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // В таблице есть столбец с именем «Столбец2», но полей MERGEFIELD с таким именем нет.
    // Кроме того, у нас есть поле MERGEFIELD с именем «Столбец3», но в источнике данных нет столбца с таким именем.
    // Если данные из «Столбца2» подходят для поля MERGEFILD «Столбец3»,
    // мы можем сопоставить имя этого столбца с MERGEFIELD в паре ключ/значение "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Мы можем связать имя столбца источника данных с именем MERGEFIELD следующим образом.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Свяжите столбец источника данных с именем «Столбец2» с MERGEFIELD с именем «Столбец3».
    mappedDataFields.Add("Column3", "Column2");

    // Имя MERGEFIELD является «ключом» к имени соответствующего столбца источника данных «значение».
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Теперь, если мы запустим это слияние почты, поля MERGEFIELD «Столбец3» будут брать данные из «Столбца2» таблицы.
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
/// Создадим документ с двумя MERGEFIELD, один из которых не имеет
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
/// Создадим таблицу данных с двумя столбцами, один из которых не имеет
/// соответствующее MERGEFIELD в исходном документе из метода выше.
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
* пространство имен [Aspose.Words.MailMerging](../../mappeddatafieldcollection/)
* сборка [Aspose.Words](../../../)


