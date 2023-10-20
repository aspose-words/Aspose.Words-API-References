---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words для .NET
description: Document UpdateFields метод. Обновляет значения полей во всем документе на С#.
type: docs
weight: 750
url: /ru/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Обновляет значения полей во всем документе.

```csharp
public void UpdateFields()
```

## Примечания

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, он сохраняет их нетронутыми. Поэтому обычно вам нужно вызвать этот метод перед сохранением, если вы изменили document программно и хотите убедиться, что правильные (вычисленные) значения полей появятся в сохраненном документе.

Нет необходимости обновлять поля после выполнения слияния почты, поскольку слияние почты является своего рода полем update и автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при визуализации документа или вызове.[`UpdatePageLayout`](../updatepagelayout/).

Использовать[`NormalizeFieldTypes`](../normalizefieldtypes/) метод перед обновлением полей, если были изменения документа, которые повлияли на типы полей.

Чтобы обновить поля в определенной части документа, используйте[`UpdateFields`](../../range/updatefields/).

## Примеры

Показывает использование поля ЦИТАТЫ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле ЦИТАТЫ, в котором будет отображаться значение свойства Text.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Вставляем поле ЦИТАТЫ и вставляем в него поле ДАТЫ.
// Поля ДАТА обновляют свое значение до текущей даты каждый раз, когда мы открываем документ с помощью Microsoft Word.
// Вложение поля ДАТА в поле ЦИТАТЫ, подобное этому, заморозит его значение
// к дате создания документа.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Обновляем все поля, чтобы отображать правильные результаты.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Показывает, как задать сведения о пользователе и отобразить их с помощью полей.

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

// Вставляем оглавление первой страницы документа.
// Настройте таблицу так, чтобы она подбирала абзацы с заголовками уровней от 1 до 3.
// Также сделайте его записи гиперссылками, которые приведут нас
// к местоположению заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Заполняем оглавление, добавляя абзацы со стилями заголовков.
// Каждый такой заголовок уровня от 1 до 3 создаст запись в таблице.
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

// Оглавление — это поле типа, которое необходимо обновить, чтобы отобразить актуальный результат.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
