---
title: FieldGreetingLine
second_title: Справочник по API Aspose.Words для .NET
description: Реализует поле GREETINGLINE.
type: docs
weight: 1830
url: /ru/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Реализует поле GREETINGLINE.

```csharp
public class FieldGreetingLine : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext) { get; set; } | Получает или задает текст для включения в поле, если имя пусто. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format) { get; } | Получает[`FieldFormat`](../fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid) { get; set; } | Получает или задает идентификатор языка, используемый для форматирования имени. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Получает или задает LCID поля. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat) { get; set; } | Получает или задает формат имени, включенного в поле. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Получает или задает текст, который находится между разделителем поля и концом поля. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Получает узел, представляющий разделитель полей. Может быть нулевым. |
| [Start](../../aspose.words.fields/field/start) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames)() | Возвращает коллекцию имен полей слияния, используемых полем. |
| [Remove](../../aspose.words.fields/field/remove)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает **нулевой** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Выполняет развязку поля. |
| [Update](../../aspose.words.fields/field/update)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Вставляет строку приветствия слияния почты.

### Примеры

Показывает, как вставить поле GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте общее приветствие, используя поле GREETINGLINE и некоторый текст после него.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Поле GREETINGLINE принимает значения из источника данных во время слияния почты, например MERGEFIELD.
// Он также может форматировать, как исходные данные записываются на свое место после завершения слияния.
// Коллекция имен полей соответствует столбцам из источника данных
// из которого поле будет принимать значения.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Чтобы заполнить этот массив, нам нужно указать формат для нашей строки приветствия.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Теперь наше поле будет принимать значения из этих двух столбцов в источнике данных.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Эта строка будет охватывать любые случаи, когда данные таблицы данных недействительны
// заменив искаженное имя строкой.
field.AlternateText = "Sir or Madam";

// Установить локаль для форматирования результата.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Создаем таблицу данных со столбцами, имена которых соответствуют элементам
// из коллекции имен полей, а затем выполнить слияние.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// Эта строка имеет недопустимое значение в столбце «Заголовок любезности», поэтому наше приветствие по умолчанию будет иметь альтернативный текст.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.That(doc.Range.Fields, Is.Empty);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Смотрите также

* class [Field](../field)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
