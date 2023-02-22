---
title: Document.UpdateFields
second_title: Справочник по API Aspose.Words для .NET
description: Document метод. Обновляет значения полей во всем документе.
type: docs
weight: 730
url: /ru/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Обновляет значения полей во всем документе.

```csharp
public void UpdateFields()
```

### Примечания

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а сохраняет их нетронутыми. правильные (вычисленные) значения полей появляются в сохраненном документе.

Нет необходимости обновлять поля после выполнения слияния, потому что слияние является своего рода полем update и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при отображении документа или вызове[`UpdatePageLayout`](../updatepagelayout/).

Использовать[`NormalizeFieldTypes`](../normalizefieldtypes/) перед обновлением полей, если в документе были изменения, влияющие на типы полей.

Для обновления полей в определенной части документа используйте[`UpdateFields`](../../range/updatefields/).

### Примеры

Показывает использование поля ЦИТАТА.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте поле QUOTE, которое будет отображать значение его свойства Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Вставляем поле ЦИТАТА и вкладываем в него поле ДАТА.
// Поля ДАТА обновляют свое значение до текущей даты каждый раз, когда мы открываем документ с помощью Microsoft Word.
// Такое вложение поля DATE внутрь поля QUOTE заморозит его значение
// до даты создания документа.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Обновляем все поля, чтобы отображались правильные результаты.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Показывает, как установить сведения о пользователе и отобразить их с помощью полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создайте объект UserInformation и установите его в качестве источника данных для полей, отображающих информацию о пользователе.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Вставляем поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
// соответствующие свойства объекта UserInformation, который мы создали выше. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Объект параметров поля также имеет статического пользователя по умолчанию, на которого могут ссылаться поля из всех документов.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Показывает, как вставить оглавление (TOC) в документ, используя стили заголовков в качестве записей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем оглавление для первой страницы документа.
// Настройте таблицу так, чтобы она выбирала абзацы с заголовками уровней от 1 до 3.
// Кроме того, установите его записи в качестве гиперссылок, которые приведут нас
// к местоположению заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Заполняем оглавление, добавляя абзацы со стилями заголовков.
// Каждый такой заголовок с уровнем от 1 до 3 создаст запись в таблице.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Оглавление — это поле типа, которое необходимо обновить для отображения актуального результата.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


