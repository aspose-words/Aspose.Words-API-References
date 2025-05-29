---
title: MailMerge.ExecuteADO
linktitle: ExecuteADO
articleTitle: ExecuteADO
second_title: Aspose.Words для .NET
description: Оптимизируйте создание документов с помощью метода MailMerge ExecuteADO. Легко объединяйте данные ADO Recordset для эффективного персонализированного вывода.
type: docs
weight: 190
url: /ru/net/aspose.words.mailmerging/mailmerge/executeado/
---
## MailMerge.ExecuteADO method

Выполняет слияние почты из объекта ADO Recordset в документ.

```csharp
public void ExecuteADO(object recordset)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| recordset | Object | Набор записей ADO или объект записи. |

## Примечания

Этот метод полезен, когда вы собираетесь использовать классы Aspose.Words как объекты COM из неуправляемого кода, например приложения, созданного с использованием ASP или Visual Basic 6.0.

Этот метод игнорируетRemoveUnusedRegions вариант.

Для получения дополнительной информации см. описание[`Execute`](../execute/).

## Примеры

```csharp
[VBScript]

Dim RS
Set RS = CreateObject("ADODB.Recordset")
RS.Open _
    "SELECT TOP 50 * FROM Customers ORDER BY Country, CompanyName", _
    "Provider=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb"

Dim License
Set License = CreateObject("Aspose.Words.License")
License.SetLicense "C:\MyPath\MyLicense.lic"

Dim Helper
Set Helper = CreateObject("Aspose.Words.ComHelper")
Dim Doc
Set Doc = Helper.Open("CustomerLabels.doc")

Doc.MailMerge.ExecuteADO RS
Doc.Save "C:\MyPath\CustomerLabels Out VBScript.doc"
```

Показывает, как выполнить слияние почты с данными из набора данных ADO.

```csharp
public void ExecuteADO()
{
    Document doc = CreateSourceDocADOMailMerge();

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
    const string command = @"SELECT ProductName, QuantityPerUnit, UnitPrice FROM Products";

    ADODB.Recordset recordset = new ADODB.Recordset();
    recordset.Open(command, connection);

    // Выполнить слияние и сохранить документ.
    doc.MailMerge.ExecuteADO(recordset);
    doc.Save(ArtifactsDir + "MailMerge.ExecuteADO.docx");
}

/// <summary>
/// Создайте пустой документ и заполните его полями MERGEFIELDS, которые будут принимать данные при выполнении слияния почты.
/// </summary>
private static Document CreateSourceDocADOMailMerge()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Product:\t");
    builder.InsertField(" MERGEFIELD ProductName");
    builder.Writeln();
    builder.InsertField(" MERGEFIELD QuantityPerUnit");
    builder.Write(" for $");
    builder.InsertField(" MERGEFIELD UnitPrice");

    return doc;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
