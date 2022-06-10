---
title: IMailMergeDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Реализуйте этот интерфейс чтобы разрешить слияние почты из пользовательского источника данных такого как список объектов. Данные Master-Detail также поддерживаются.
type: docs
weight: 3540
url: /ru/net/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface

Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, такого как список объектов. Данные Master-Detail также поддерживаются.

```csharp
public interface IMailMergeDataSource
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [TableName](../../aspose.words.mailmerging/imailmergedatasource/tablename) { get; } | Возвращает имя источника данных. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetChildDataSource](../../aspose.words.mailmerging/imailmergedatasource/getchilddatasource)(string) | Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния почты. |
| [GetValue](../../aspose.words.mailmerging/imailmergedatasource/getvalue)(string, out object) | Возвращает значение для указанного имени поля или false, если поле не найдено. |
| [MoveNext](../../aspose.words.mailmerging/imailmergedatasource/movenext)() | Переход к следующей записи в источнике данных. |

### Примечания

Когда создается источник данных, он должен быть инициализирован так, чтобы он указывал на BOF (до первого записывать). Механизм слияния почты Aspose.Words вызовет[`MoveNext`](./movenext)для перехода к следующей записи и затем вызовет[`GetValue`](./getvalue)для каждого поля слияния, которое встречается в документе или в текущей области слияния.

### Примеры

Показывает, как выполнить слияние почты с источник данных в виде пользовательского объекта.

```csharp
public void CustomDataSource()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(" MERGEFIELD FullName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    List<Customer> customers = new List<Customer>();
    customers.Add(new Customer("Thomas Hardy", "120 Hanover Sq., London"));
    customers.Add(new Customer("Paolo Accorti", "Via Monte Bianco 34, Torino"));

     // Чтобы использовать пользовательский объект в качестве источника данных, он должен реализовать интерфейс IMailMergeDataSource. 
    CustomerMailMergeDataSource dataSource = new CustomerMailMergeDataSource(customers);

    doc.MailMerge.Execute(dataSource);

    doc.Save(ArtifactsDir + "MailMergeCustom.CustomDataSource.docx");
}

/// <summary>
 /// Пример класса "объект данных" в вашем приложении.
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
 /// Пользовательский источник данных слияния, который вы реализуете, чтобы разрешить Aspose.Words 
/// для отправки данных слияния из ваших объектов Customer в документы Microsoft Word.
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
     /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми регионами.
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
                 // Возвращаем "false" механизму слияния почты Aspose.Words для signify
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

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
