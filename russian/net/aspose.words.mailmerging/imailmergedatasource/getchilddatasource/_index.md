---
title: IMailMergeDataSource.GetChildDataSource
linktitle: GetChildDataSource
articleTitle: GetChildDataSource
second_title: Aspose.Words для .NET
description: Узнайте, как метод GetChildDataSource от IMailMergeDataSource улучшает слияние почты Aspose.Words, легко управляя вложенными областями.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource.GetChildDataSource method

Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния почты.

```csharp
public IMailMergeDataSource GetChildDataSource(string tableName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | String | Имя региона слияния почты, указанное в шаблоне документа. Без учета регистра. |

### Возвращаемое значение

Объект источника данных, который обеспечит доступ к записям данных указанной таблицы.

## Примечания

Когда движки слияния почты Aspose.Words заполняют область слияния почты данными и обнаруживают начало вложенной области слияния почты в форме MERGEFIELD TableStart:TableName, он вызывает`GetChildDataSource` на объекте источника данных current . Ваша реализация должна возвращать новый объект источника данных, который предоставит доступ к записям child текущей родительской записи. Aspose.Words будет использовать возвращенный источник данных для заполнения вложенной области слияния почты.

Ниже приведены правила, которым должна соответствовать реализация`GetChildDataSource` должен следовать.

Если таблица, представленная этим объектом источника данных, имеет связанную дочернюю (подробную) таблицу с указанным именем , то ваша реализация должна возвращать новый[`IMailMergeDataSource`](../) объект, который предоставит access для дочерних записей текущей записи. Примером этого является отношение Orders / OrderDetails. Предположим, что текущая[`IMailMergeDataSource`](../) object представляет таблицу Orders и имеет текущую запись заказа. Далее Aspose.Words встречает "MERGEFIELD TableStart:OrderDetails" в документе и вызывает`GetChildDataSource` . Вам необходимо создать и вернуть[`IMailMergeDataSource`](../) Объект , который позволит Aspose.Words получить доступ к записи OrderDetails для текущего заказа.

Если этот объект источника данных не имеет отношения к таблице с указанным именем, то необходимо вернуть [`IMailMergeDataSource`](../)объект, который предоставит доступ ко всем записям указанной таблицы.

Если таблица с указанным именем не существует, ваша реализация должна вернуть`нулевой` .

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

* interface [IMailMergeDataSource](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
