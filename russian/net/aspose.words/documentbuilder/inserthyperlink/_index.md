---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: Aspose.Words для .NET
description: Улучшайте свои документы с помощью метода InsertHyperlink в DocumentBuilder, легко добавляя кликабельные ссылки для улучшения навигации и взаимодействия с пользователем.
type: docs
weight: 390
url: /ru/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

Вставляет гиперссылку в документ.

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | String | Текст ссылки, который будет отображаться в документе. |
| urlOrBookmark | String | Назначение ссылки. Может быть URL-адресом или именем закладки внутри документа. Этот метод всегда добавляет апострофы в начале и конце URL-адреса. |
| isBookmark | Boolean | `истинный` если предыдущий параметр — имя закладки внутри документа; `ЛОЖЬ` предыдущий параметр — это URL. |

### Возвращаемое значение

А[`Field`](../../../aspose.words.fields/field/) объект, представляющий вставленное поле.

## Примечания

Обратите внимание, что вам необходимо указать форматирование шрифта для отображаемого текста гиперссылки explicitly с помощью[`Font`](../font/) свойство.

Этот метод внутренне вызывает[`InsertField`](../insertfield/)для вставки ГИПЕРССЫЛКИ MS Word field в документ.

## Примеры

Показывает, как вставить поле гиперссылки.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Вставьте гиперссылку и выделите ее с помощью пользовательского форматирования.
// Гиперссылка будет представлять собой фрагмент текста, нажав на который, мы перейдем в место, указанное в URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", ложь);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word перенаправит нас на URL-адрес через новое окно веб-браузера.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

Показывает, как вставить гиперссылку, ссылающуюся на локальную закладку.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// Вставьте поле HYPERLINK, которое ссылается на закладку. Мы можем передавать переключатели полей
// в метод "InsertHyperlink" как часть аргумента, содержащего имя указанной закладки.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
FieldHyperlink hyperlink = (FieldHyperlink)builder.InsertHyperlink("Link to Bookmark1", "Bookmark1", true);
hyperlink.ScreenTip = "Hyperlink Tip";

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

Показывает, как использовать стек форматирования конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте форматирование шрифта, затем напишите текст, который будет перед гиперссылкой.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Сохраняем текущую конфигурацию форматирования в стеке.
builder.PushFont();

// Измените текущее форматирование конструктора, применив новый стиль.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", ложь);

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
