---
title: Font.Underline
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает тип подчеркивания применяемого к шрифту.
type: docs
weight: 530
url: /ru/net/aspose.words/font/underline/
---
## Font.Underline property

Получает или задает тип подчеркивания, применяемого к шрифту.

```csharp
public Underline Underline { get; set; }
```

### Примеры

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

// Вставьте гиперссылку и подчеркните ее с помощью специального форматирования.
// Гиперссылка будет интерактивным фрагментом текста, который приведет нас к месту, указанному в URL-адресе.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + щелчок левой кнопкой мыши по ссылке в тексте в Microsoft Word приведет нас к URL-адресу через новое окно веб-браузера.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Смотрите также

* enum [Underline](../../underline/)
* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


