---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words для .NET
description: Восстановите свой текст в его первоначальном стиле с помощью метода Font ClearFormatting. Наслаждайтесь чистым, последовательным форматированием для безупречного вида!
type: docs
weight: 560
url: /ru/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Сбрасывает форматирование шрифта до значения по умолчанию.

```csharp
public void ClearFormatting()
```

## Примечания

Удаляет все форматирование шрифта, явно указанное для объекта, из which [`Font`](../) был получен, поэтому форматирование шрифта будет унаследовано от соответствующего родителя.

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

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
