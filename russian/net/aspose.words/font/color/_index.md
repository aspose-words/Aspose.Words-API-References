---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words для .NET
description: Font Color свойство. Получает или задает цвет шрифта на С#.
type: docs
weight: 70
url: /ru/net/aspose.words/font/color/
---
## Font.Color property

Получает или задает цвет шрифта.

```csharp
public Color Color { get; set; }
```

## Примеры

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

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
