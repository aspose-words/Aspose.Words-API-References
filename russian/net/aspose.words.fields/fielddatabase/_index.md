---
title: Class FieldDatabase
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldDatabase сорт. Реализует поле БАЗЫ ДАННЫХ.
type: docs
weight: 1740
url: /ru/net/aspose.words.fields/fielddatabase/
---
## FieldDatabase class

Реализует поле БАЗЫ ДАННЫХ.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

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
| [Connection](../../aspose.words.fields/fielddatabase/connection/) { get; set; } | Получает или устанавливает соединение с данными. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [FileName](../../aspose.words.fields/fielddatabase/filename/) { get; set; } | Получает или задает полный путь и имя файла базы данных . |
| [FirstRecord](../../aspose.words.fields/fielddatabase/firstrecord/) { get; set; } | Получает или задает целочисленный номер первой вставляемой записи данных. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [FormatAttributes](../../aspose.words.fields/fielddatabase/formatattributes/) { get; set; } | Получает или задает атрибуты формата, которые следует применить к таблице. |
| [InsertHeadings](../../aspose.words.fields/fielddatabase/insertheadings/) { get; set; } | Получает или задает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующую таблицу. |
| [InsertOnceOnMailMerge](../../aspose.words.fields/fielddatabase/insertonceonmailmerge/) { get; set; } | Получает или задает необходимость вставки данных в начале слияния. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LastRecord](../../aspose.words.fields/fielddatabase/lastrecord/) { get; set; } | Получает или задает целый номер последней вставляемой записи данных. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [Query](../../aspose.words.fields/fielddatabase/query/) { get; set; } | Получает или задает набор инструкций SQL, которые запрашивают базу данных. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| [TableFormat](../../aspose.words.fields/fielddatabase/tableformat/) { get; set; } | Получает или задает формат, который будет применен к результату запроса к базе данных. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет результаты запроса к базе данных в таблицу WordprocessingML.

### Примеры

Показывает, как извлечь данные из базы данных и вставить их как поле в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Это поле DATABASE будет выполнять запрос к базе данных и отображать результат в таблице.
FieldDatabase field = (FieldDatabase)builder.InsertField(FieldType.FieldDatabase, true);
field.FileName = DatabaseDir + "Northwind.accdb";
field.Connection = "Provider=Microsoft.ACE.OLEDB.12.0";
field.Query = "SELECT * FROM [Products]";

Assert.AreEqual($" DATABASE  \\d {DatabaseDir.Replace("\\", "\\\\") + "Northwind.accdb"} \\c Provider=Microsoft.ACE.OLEDB.12.0 \\s \"SELECT * FROM [Products]\"", field.GetFieldCode());

// Вставьте еще одно поле БАЗЫ ДАННЫХ с более сложным запросом, который сортирует все продукты в порядке убывания валового объема продаж.
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
// Настройте их для отображения только строк с 1 по 10 результата запроса в таблице полей.
field.FirstRecord = "1";
field.LastRecord = "10";

// Это свойство является индексом формата, который мы хотим использовать для нашей таблицы. Список форматов таблиц находится в меню «Автоформат таблицы...».
// которое появляется, когда мы создаем поле БАЗЫ ДАННЫХ в Microsoft Word. Индекс №10 соответствует формату «Цветной 3».
field.TableFormat = "10";

// Свойство FormatAttribute — это строковое представление целого числа, которое хранит несколько флагов.
// Мы можем индивидуально применить формат, на который указывает свойство TableFormat, установив в этом свойстве разные флаги.
// Используемое нами число представляет собой сумму комбинации значений, соответствующих различным аспектам стиля таблицы.
// 63 представляет собой 1 (границы) + 2 (затенение) + 4 (шрифт) + 8 (цвет) + 16 (автоподбор) + 32 (строки заголовков).
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


