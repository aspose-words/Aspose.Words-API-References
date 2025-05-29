---
title: FieldGreetingLine.NameFormat
linktitle: NameFormat
articleTitle: NameFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FieldGreetingLine NameFormat, чтобы легко настраивать форматы имен в полях, улучшая пользовательский опыт и персонализацию.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldgreetingline/nameformat/
---
## FieldGreetingLine.NameFormat property

Возвращает или задает формат имени, включенного в поле.

```csharp
public string NameFormat { get; set; }
```

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

* class [FieldGreetingLine](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
