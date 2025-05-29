---
title: FieldGreetingLine Class
linktitle: FieldGreetingLine
articleTitle: FieldGreetingLine
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldGreetingLine, предназначенный для простой реализации полей GREETINGLINE для расширенной персонализации документов.
type: docs
weight: 2390
url: /ru/net/aspose.words.fields/fieldgreetingline/
---
## FieldGreetingLine class

Реализует поле GREETINGLINE.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldGreetingLine : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldGreetingLine](fieldgreetingline/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AlternateText](../../aspose.words.fields/fieldgreetingline/alternatetext/) { get; set; } | Возвращает или задает текст, который необходимо включить в поле, если имя пустое. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LanguageId](../../aspose.words.fields/fieldgreetingline/languageid/) { get; set; } | Возвращает или задает идентификатор языка, используемый для форматирования имени. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [NameFormat](../../aspose.words.fields/fieldgreetingline/nameformat/) { get; set; } | Возвращает или задает формат имени, включенного в поле. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [GetFieldNames](../../aspose.words.fields/fieldgreetingline/getfieldnames/)() | Возвращает коллекцию имен полей слияния, используемых полем. |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Вставляет строку приветствия для слияния писем.

## Примеры

Показывает, как вставить поле GREETINGLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте общее приветствие, используя поле GREETINGLINE и текст после него.
FieldGreetingLine field = (FieldGreetingLine)builder.InsertField(FieldType.FieldGreetingLine, true);
builder.Writeln("\n\n\tThis is your custom greeting, created programmatically using Aspose Words!");

// Поле GREETINGLINE принимает значения из источника данных во время слияния почты, как MERGEFIELD.
// Он также может форматировать способ записи данных источника на свое место после завершения слияния почты.
// Коллекция имен полей соответствует столбцам из источника данных
// из которого поле будет брать значения.
Assert.AreEqual(0, field.GetFieldNames().Length);

// Чтобы заполнить этот массив, нам нужно указать формат нашей строки приветствия.
field.NameFormat = "<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> ";

// Теперь наше поле будет принимать значения из этих двух столбцов в источнике данных.
Assert.AreEqual("Courtesy Title", field.GetFieldNames()[0]);
Assert.AreEqual("Last Name", field.GetFieldNames()[1]);
Assert.AreEqual(2, field.GetFieldNames().Length);

// Эта строка будет охватывать все случаи, когда данные таблицы данных недействительны
// заменив неверно сформированное имя строкой.
field.AlternateText = "Sir or Madam";

// Задайте локаль для форматирования результата.
field.LanguageId = new CultureInfo("en-US").LCID.ToString();

Assert.AreEqual(" GREETINGLINE  \\f \"<< _BEFORE_ Dear >><< _TITLE0_ >><< _LAST0_ >><< _AFTER_ ,>> \" \\e \"Sir or Madam\" \\l 1033", 
    field.GetFieldCode());

// Создаем таблицу данных со столбцами, имена которых соответствуют элементам
// из коллекции имен полей поля, а затем выполнить слияние почты.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// В этой строке указано недопустимое значение в столбце «Заголовок любезности», поэтому по умолчанию в качестве приветствия будет использоваться альтернативный текст.
table.Rows.Add("", "No", "Name");

doc.MailMerge.Execute(table);

Assert.AreEqual(0, doc.Range.Fields.Count);
Assert.AreEqual("Dear Mr. Doe,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Mrs. Cardholder,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!\r" +
                "\fDear Sir or Madam,\r\r\tThis is your custom greeting, created programmatically using Aspose Words!",
    doc.GetText().Trim());
```

### Смотрите также

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
