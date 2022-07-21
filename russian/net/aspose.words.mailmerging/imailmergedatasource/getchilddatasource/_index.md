---
title: GetChildDataSource
second_title: Справочник по API Aspose.Words для .NET
description: Механизм слияния Aspose.Words вызывает этот метод когда обнаруживает начало вложенной области слияния.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Механизм слияния Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | String | Имя региона слияния, указанное в шаблоне документа. Без учета регистра. |

### Возвращаемое значение

Объект источника данных, который предоставит доступ к записям данных указанной таблицы.

### Примечания

Когда механизмы слияния почты Aspose.Words заполняют область слияния данными и обнаруживают начало области слияния nested в форме MERGEFIELD TableStart:TableName, он вызывает`GetChildDataSource` в объекте источника данных current . Ваша реализация должна вернуть новый объект источника данных, который обеспечит доступ к записям child текущей родительской записи. Aspose.Words будет использовать возвращенный источник данных для заполнения вложенной области слияния почты.

Ниже приведены правила реализации`GetChildDataSource` должен следовать.

Если таблица, представленная этим объектом источника данных, имеет связанную дочернюю (подробную) таблицу с указанным именем, , тогда ваша реализация должна вернуть новый[`IMailMergeDataSource`](../../imailmergedatasource) объект, который предоставит доступ к дочерним записям текущей записи. Примером этого является отношение Orders / OrderDetails. Предположим, что текущий[`IMailMergeDataSource`](../../imailmergedatasource) object представляет таблицу Orders и имеет текущую запись заказа. Затем Aspose.Words обнаруживает в документе «MERGEFIELD TableStart:OrderDetails» и вызывает`GetChildDataSource` . Вам нужно создать и вернуть[`IMailMergeDataSource`](../../imailmergedatasource) объект, который позволит Aspose.Words получить доступ к записи OrderDetails для текущего заказа.

Если этот объект источника данных не имеет отношения к таблице с указанным именем, то необходимо вернуть a[`IMailMergeDataSource`](../../imailmergedatasource)объект, который предоставит доступ ко всем записям указанной таблицы.

Если таблица с указанным именем не существует, ваша реализация должна вернуть`нулевой` .

### Примеры

Показывает, как выполнить слияние с источником данных в виде пользовательского объекта.

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
/// Пользовательский источник данных слияния, который вы реализуете, чтобы позволить Aspose.Words 
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
    /// Имя источника данных. Используется Aspose.Words только при выполнении слияния почты с повторяемыми областями.
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
                // Возвращаем "false" механизму слияния почты Aspose.Words, чтобы обозначить
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

* interface [IMailMergeDataSource](../../imailmergedatasource)
* пространство имен [Aspose.Words.MailMerging](../../imailmergedatasource)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
