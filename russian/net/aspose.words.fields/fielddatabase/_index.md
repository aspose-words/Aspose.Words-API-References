---
title: FieldDatabase Class
linktitle: FieldDatabase
articleTitle: FieldDatabase
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldDatabase для эффективной реализации полей DATABASE в ваших документах. Улучшите автоматизацию документов сегодня!
type: docs
weight: 2150
url: /ru/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Реализует поле DATABASE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldDatabase : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldDatabase](fielddatabase/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Получает или задает соединение с данными. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Возвращает или задает полный путь и имя файла базы данных |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Возвращает или задает целочисленный номер первой записи данных для вставки. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Возвращает или задает атрибуты формата, которые должны быть применены к таблице. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Возвращает или задает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Возвращает или задает, следует ли вставлять данные в начале слияния. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Возвращает или задает целочисленный номер последней записи данных для вставки. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Возвращает или задает набор инструкций SQL, которые запрашивают базу данных. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Возвращает или задает формат, который должен применяться к результату запроса к базе данных. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Вставляет результаты запроса базы данных в таблицу WordprocessingML.

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

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
