---
title: Font.ClearFormatting
second_title: Справочник по API Aspose.Words для .NET
description: Font метод. Сбрасывает формат шрифта по умолчанию.
type: docs
weight: 550
url: /ru/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Сбрасывает формат шрифта по умолчанию.

```csharp
public void ClearFormatting()
```

### Примечания

Удаляет все форматирование шрифта, явно указанное для объекта, из которого [`Font`](../) был получен, поэтому форматирование шрифта будет унаследовано от соответствующего родительского элемента.

### Примеры

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
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


