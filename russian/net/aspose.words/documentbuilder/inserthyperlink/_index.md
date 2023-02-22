---
title: DocumentBuilder.InsertHyperlink
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет гиперссылку в документ.
type: docs
weight: 340
url: /ru/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Вставляет гиперссылку в документ.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | String | Текст ссылки для отображения в документе. |
| urlOrBookmark | String | Назначение ссылки. Может быть URL-адресом или именем закладки внутри документа. Этот метод всегда добавляет апострофы в начале и конце URL-адреса. |
| isBookmark | Boolean | Истинно, если предыдущий параметр является именем закладки внутри документа; ложь, если предыдущий параметр является URL-адресом. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

### Примечания

Обратите внимание, что форматирование шрифта для отображаемого текста гиперссылки необходимо указать явно с помощью параметра[`Font`](../font/) имущество.

Этот метод вызывает внутренние вызовы[`InsertField`](../insertfield/) чтобы вставить в документ ГИПЕРССЫЛКУ MS Word field .

### Примеры

Показывает, как вставить гиперссылку, ссылающуюся на локальную закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Вставьте поле ГИПЕРССЫЛКИ, которое ссылается на закладку. Мы можем передать полевые переключатели
// в метод "InsertHyperlink" как часть аргумента, содержащего имя закладки, на которую делается ссылка.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Показывает, как вставить поле гиперссылки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Вставьте гиперссылку и подчеркните ее с помощью пользовательского форматирования.
// Гиперссылка будет кликабельным фрагментом текста, который приведет нас к месту, указанному в URL-адресе.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word приведет нас к URL-адресу через новое окно веб-браузера.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Показывает, как использовать стек форматирования конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте форматирование шрифта, затем напишите текст перед гиперссылкой.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Сохраняем нашу текущую конфигурацию форматирования в стеке.
builder.PushFont();

// Изменить текущее форматирование построителя, применив новый стиль.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Восстанавливаем форматирование шрифта, которое мы сохранили ранее, и удаляем элемент из стека.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Смотрите также

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


