---
title: ExecuteWithRegionsADO
second_title: Справочник по API Aspose.Words для .NET
description: Выполняет слияние почты из объекта набора записей ADO в документ с областями слияния.
type: docs
weight: 210
url: /ru/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Выполняет слияние почты из объекта набора записей ADO в документ с областями слияния.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| recordset | Object | Набор записей ADO или объект записи. |
| tableName | String | Имя области слияния в документе для заполнения. |

### Примечания

Этот метод полезен, когда вы собираетесь использовать классы Aspose.Words как COM-объекты из неуправляемого кода, такого как приложение, созданное с использованием ASP или Visual Basic 6.0.

Дополнительные сведения см. в описании MailMerge.ExecuteWithRegions(DataTable).

### Примеры

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

     // Для работы с наборами данных ADO нам потребуется добавить ссылку на библиотеку Microsoft ActiveX Data Objects, 
     // который включен в дистрибутив .NET и хранится в "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

     // Создаем строку подключения, указывающую на базу данных "Борей" file
     // в нашей локальной файловой системе и открываем соединение.
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

     // Заполняем наш набор данных, запустив команду SQL в нашей базе данных.
     // Имена столбцов в таблице результатов должны соответствовать
     // к значениям MERGEFIELDS, которые будут вмещать наши данные.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Запускаем слияние только для первого региона, заполняя его MERGEFIELDS данными из набора записей.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

     // Закрываем набор записей и снова открываем его с данными из другого SQL-запроса.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

     // Запускаем второе слияние во втором регионе и сохраняем документ.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");
}

/// <summary>
 /// Создать документ с двумя областями слияния.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

Показывает, как выполнить слияние почты с несколькими регионами, скомпилированными с данными из набора данных ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

     // Для работы с наборами данных ADO нам потребуется добавить ссылку на библиотеку Microsoft ActiveX Data Objects, 
     // который включен в дистрибутив .NET и хранится в "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

     // Создаем строку подключения, указывающую на базу данных "Борей" file
     // в нашей локальной файловой системе и открываем соединение.
    string connectionString = @"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=" + DatabaseDir + "Northwind.mdb";
    connection.Open(connectionString);

     // Заполняем наш набор данных, запустив команду SQL в нашей базе данных.
     // Имена столбцов в таблице результатов должны соответствовать
     // к значениям MERGEFIELDS, которые будут вмещать наши данные.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Запускаем слияние только для первого региона, заполняя его MERGEFIELDS данными из набора записей.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

     // Закрываем набор записей и снова открываем его с данными из другого SQL-запроса.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

     // Запускаем второе слияние во втором регионе и сохраняем документ.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");
}

/// <summary>
 /// Создать документ с двумя областями слияния.
/// </summary>
private static Document CreateSourceDocADOMailMergeWithRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("\tEmployees: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion1");
    builder.InsertField(" MERGEFIELD FirstName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD LastName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion1");
    builder.InsertParagraph();

    builder.Writeln("\tCustomers: ");
    builder.InsertField(" MERGEFIELD TableStart:MergeRegion2");
    builder.InsertField(" MERGEFIELD ContactName");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Address");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD City");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion2");

    return doc;
}
```

### Смотрите также

* class [MailMerge](../../mailmerge)
* namespace [Aspose.Words.MailMerging](../../mailmerge)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
