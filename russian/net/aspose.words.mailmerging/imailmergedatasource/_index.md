---
title: IMailMergeDataSource Interface
linktitle: IMailMergeDataSource
articleTitle: IMailMergeDataSource
second_title: Aspose.Words для .NET
description: Откройте для себя мощные возможности слияния почты с Aspose.Words.MailMerging.IMailMergeDataSource. Легко подключайте пользовательские источники данных для бесперебойной автоматизации документов.
type: docs
weight: 4500
url: /ru/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, например, списка объектов. Также поддерживаются данные Master-detail.

```csharp
public interface IMailMergeDataSource
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename/) { get; } | Возвращает имя источника данных. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource/)(*string*) | Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния почты. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue/)(*string, out object*) | Возвращает значение для указанного имени поля или`ЛОЖЬ` если поле не найдено. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext/)() | Переход к следующей записи в источнике данных. |

## Примечания

При создании источника данных его следует инициализировать так, чтобы он указывал на BOF (до первой записи). Механизм слияния почты Aspose.Words вызовет[`MoveNext`](./movenext/) для перехода к следующей записи and затем вызвать[`GetValue`](./getvalue/) для каждого поля слияния, встречающегося в документе или в текущей области слияния.

## Примеры

Показывает, как выполнить слияние почты с источником данных в виде пользовательского объекта.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>
    {
        new Customer("Thomas Hardy", "120 Hanover Sq., London"),
        new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino")
    };

     // Чтобы использовать пользовательский объект в качестве источника данных, он должен реализовывать интерфейс IMailMergeDataSource.
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
/// Пример класса «сущность данных» в вашем приложении.
/// </summary>
public class Customer
{
    public Customer(string aFullName, string anAddress)
    {
        FullName = aFullName;
        Address = anAddress;
    }

    public string FullName { get; set; }
    public string Address { get; set; }
}

/// <summary>
 /// Пользовательский источник данных для слияния почты, который вы реализуете, чтобы разрешить Aspose.Words
/// для слияния данных из объектов Customer в документы Microsoft Word.
/// </summary>
public class CustomerMailMergeDataSource : IMailMergeDataSource
{
    public CustomerMailMergeDataSource(List<Customer> customers)
    {
        mCustomers = customers;

        // Когда мы инициализируем источник данных, его позиция должна быть перед первой записью.
        mRecordIndex = -1;
    }

    /// <summary>
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяющимися регионами.
    /// </summary>
    public string TableName
    {
        get { return "Customer"; }
    }

    /// <summary>
    /// Aspose.Words вызывает этот метод, чтобы получить значение для каждого поля данных.
    /// </summary>
    public bool GetValue(string fieldName, out object fieldValue)
    {
        switch (fieldName)
        {
            case "FullName":
                fieldValue = mCustomers[mRecordIndex].FullName;
                return true;
            case "Address":
                fieldValue = mCustomers[mRecordIndex].Address;
                return true;
            default:
                // Возвращаем "false" в движок слияния почты Aspose.Words, чтобы обозначить
                // что мы не смогли найти поле с таким именем.
                fieldValue = null;
                return false;
        }
    }

    /// <summary>
    /// Стандартная реализация перехода к следующей записи в коллекции.
    /// </summary>
    public bool MoveNext()
    {
        if (!IsEof)
            mRecordIndex++;

        return !IsEof;
    }

    public IMailMergeDataSource GetChildDataSource(string tableName)
    {
        return null;
    }

    private bool IsEof
    {
        get { return (mRecordIndex >= mCustomers.Count); }
    }

    private readonly List<Customer> mCustomers;
    private int mRecordIndex;
}
```

### Смотрите также

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
