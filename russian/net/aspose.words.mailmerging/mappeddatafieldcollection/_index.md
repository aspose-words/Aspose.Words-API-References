---
title: MappedDataFieldCollection
second_title: Справочник по API Aspose.Words для .NET
description: Позволяет автоматически сопоставлять имена полей в вашем источнике данных и имена полей слияния в документе.
type: docs
weight: 3600
url: /ru/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Позволяет автоматически сопоставлять имена полей в вашем источнике данных и имена полей слияния в документе.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count) { get; } | Получает количество элементов, содержащихся в коллекции. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item) { get; set; } | Получает или задает имя поля в источнике данных, связанном с указанным полем слияния. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add)(string, string) | Добавляет новое сопоставление полей. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear)() | Удаляет все элементы из коллекции. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey)(string) | Определяет, существует ли в коллекции отображение из указанного поля в документе. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue)(string) | Определяет, существует ли в коллекции сопоставление из указанного поля в источнике данных. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator)() | Возвращает объект перечислителя словаря, который можно использовать для перебора всех элементов коллекции. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove)(string) | Удаляет сопоставление полей. |

### Примечания

Это реализовано как набор строковых ключей в строковые значения. Ключи — это имена полей слияния в документе, а значения — это имена полей в вашем источнике данных.

### Примеры

Показывает, как сопоставлять столбцы данных и поля MERGEFIELD с разными именами, чтобы данные передавались между ними во время слияния почты.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

     // В таблице есть столбец с именем "Column2", но нет полей MERGEFIELD с таким именем.
     // Кроме того, у нас есть поле MERGEFIELD с именем "Column3", но в источнике данных нет столбца с таким именем.
     // Если данные из "Столбца2" подходят для "Столбца3" MERGEFIELD,
     // мы можем сопоставить имя этого столбца с MERGEFIELD в паре ключ/значение MappedDataFields.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

     // Мы можем связать имя столбца источника данных с именем MERGEFIELD следующим образом.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

     // Свяжите столбец источника данных с именем "Column2" с MERGEFIELD с именем "Column3".
    mappedDataFields.Add("Column3", "Column2");

     // Имя MERGEFIELD является «ключом» к соответствующему имени столбца источника данных «value».
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

     // Теперь, если мы запустим это слияние почты, поля MERGEFIELD "Column3" будут брать данные из "Column2" таблицы.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Мы можем перебирать элементы в этой коллекции.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

     // Мы также можем удалить элементы из коллекции.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
 /// Создаем документ с 2 MERGEFIELD, в одном из которых нет a
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
 /// Создаем таблицу данных с 2 столбцами, один из которых не имеет a
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

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
