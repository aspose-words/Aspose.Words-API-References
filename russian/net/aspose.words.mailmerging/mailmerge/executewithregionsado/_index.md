---
title: MailMerge.ExecuteWithRegionsADO
linktitle: ExecuteWithRegionsADO
articleTitle: ExecuteWithRegionsADO
second_title: Aspose.Words для .NET
description: Оптимизируйте создание документов с помощью метода MailMerge ExecuteWithRegionsADO. Легко объединяйте данные ADO Recordset для персонализированных результатов.
type: docs
weight: 210
url: /ru/net/aspose.words.mailmerging/mailmerge/executewithregionsado/
---
## MailMerge.ExecuteWithRegionsADO method

Выполняет слияние почты из объекта ADO Recordset в документ с областями слияния почты.

```csharp
public void ExecuteWithRegionsADO(object recordset, string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| recordset | Object | Набор записей ADO или объект записи. |
| tableName | String | Имя области слияния в документе, которую необходимо заполнить. |

## Примечания

Этот метод полезен, когда вы собираетесь использовать классы Aspose.Words как объекты COM из неуправляемого кода, например приложения, созданного с использованием ASP или Visual Basic 6.0.

Для получения дополнительной информации см. описание[`ExecuteWithRegions`](../executewithregions/).

## Примеры

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT * FROM AsposeWordOrderDetails WHERE OrderId = 10444 ORDER BY ProductID", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")

Dim Doc
Set Doc = Helper.Open("Invoice.doc")

Doc.MailMerge.ExecuteWithRegionsADO RS, "OrderDetails"
Doc.Save "Invoice Out VBScript.doc"
```

Показывает, как выполнить слияние почты с несколькими регионами, скомпилированными с данными из набора данных ADO.

```csharp
public void ExecuteWithRegionsADO()
{
    Document doc = CreateSourceDocADOMailMergeWithRegions();

    // Для работы с ADO DataSets нам потребуется добавить ссылку на библиотеку Microsoft ActiveX Data Objects,
    // который включен в дистрибутив .NET и хранится в "adodb.dll".
    ADODB.Connection connection = new ADODB.Connection();

    // Создаем строку подключения, указывающую на файл базы данных «Northwind»
    // в нашей локальной файловой системе и открываем соединение.
    string connectionString = @"Provider=Microsoft.ACE.OLEDB.12.0;Data Source=" + DatabaseDir + "Northwind.accdb";
    connection.Open(connectionString);

    // Заполняем наш DataSet, выполнив команду SQL в нашей базе данных.
    // Имена столбцов в таблице результатов должны соответствовать
    // к значениям MERGEFIELDS, которые будут содержать наши данные.
    string command = "SELECT FirstName, LastName, City FROM Employees";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Запускаем слияние только для первого региона, заполняя его MERGEFIELDS данными из набора записей.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion1");

    // Закрываем набор записей и открываем его заново с данными из другого SQL-запроса.
    command = "SELECT * FROM Customers";

    recordset.Close();
    recordset.Open(command, connection);

    // Запускаем второе слияние почты во втором регионе и сохраняем документ.
    doc.MailMerge.ExecuteWithRegionsADO(recordset, "MergeRegion2");

    doc.Save(ArtifactsDir + "MailMerge.ExecuteWithRegionsADO.docx");

}

/// <summary>
/// Создайте документ с двумя областями слияния почты.
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

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
