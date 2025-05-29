---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetQueryResult от IFieldDatabaseProvider для эффективного извлечения данных. Оптимизируйте свои запросы и улучшите производительность базы данных уже сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Возвращает результат запроса.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь и имя файла базы данных, указанные в переключателе поля \d. |
| connection | String | Подключение к данным, указанным в поле \c switch. |
| query | String | Набор инструкций SQL, которые запрашивают базу данных, указанную в переключателе поля \s. |
| field | FieldDatabase | Поле обновляется. |

### Возвращаемое значение

The[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) экземпляр, который следует использовать для обновления поля.

## Примеры

Показывает, как извлечь данные из базы данных и вставить их в качестве поля в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Это поле DATABASE выполнит запрос к базе данных и отобразит результат в таблице.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Вставьте еще одно поле БАЗЫ ДАННЫХ с более сложным запросом, который сортирует все продукты в порядке убывания валовых продаж.
field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query =
    "SELECT [Products].ProductName, FORMAT(SUM([Order Details].UnitPrice * (1 - [Order Details].Discount) * [Order Details].Quantity), 'Currency') AS GrossSales " +
    "FROM([Products] " +
    "LEFT JOIN[Order Details] ON[Products].[ProductID] = [Order Details].[ProductID]) " +
    "GROUP BY[Products].ProductName " +
    "ORDER BY SUM([Order Details].UnitPrice* (1 - [Order Details].Discount) * [Order Details].Quantity) DESC";

// Эти свойства имеют ту же функцию, что и предложения LIMIT и TOP.
// Настройте их для отображения только строк с 1 по 10 результата запроса в таблице поля.
field.FirstRecord = "1";
field.LastRecord = "10";

// Это свойство — индекс формата, который мы хотим использовать для нашей таблицы. Список форматов таблиц находится в меню "Автоформат таблицы..."
// который появляется, когда мы создаем поле БАЗЫ ДАННЫХ в Microsoft Word. Индекс № 10 соответствует формату "Colorful 3".
field.TableFormat = "10";

// Свойство FormatAttribute — это строковое представление целого числа, которое хранит несколько флагов.
// Мы можем частично применить формат, на который указывает свойство TableFormat, установив различные флаги в этом свойстве.
// Число, которое мы используем, представляет собой сумму комбинации значений, соответствующих различным аспектам стиля таблицы.
// 63 представляет 1 (границы) + 2 (затенение) + 4 (шрифт) + 8 (цвет) + 16 (автоподбор) + 32 (строки заголовков).
field.FormatAttributes = "63";
field.InsertHeadings = true;
field.InsertOnceOnMailMerge = true;

doc.FieldOptions.FieldDatabaseProvider = new OleDbFieldDatabaseProvider();
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.DATABASE.docx");
```

### Смотрите также

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
