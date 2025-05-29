---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Underline для настройки стилей текста. Легко устанавливайте и изменяйте типы подчеркивания для улучшения типографики в ваших проектах.
type: docs
weight: 540
url: /ru/net/aspose.words/font/underline/
---
## Font.Underline property

Возвращает или задает тип подчеркивания, применяемого к шрифту.

```csharp
public Underline Underline { get; set; }
```

## Примеры

Показывает, как настроить стиль и цвет подчеркивания текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Показывает, как вставлять форматированный текст с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите форматирование шрифта, затем добавьте текст.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

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

* enum [Underline](../../underline/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
