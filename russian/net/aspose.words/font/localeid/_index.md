---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words для .NET
description: Узнайте, как свойство Font LocaleId улучшает форматирование текста, управляя идентификаторами локалей для различных языков символов. Улучшите свой код сегодня!
type: docs
weight: 200
url: /ru/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Возвращает или задает идентификатор локали (язык) форматируемых символов.

```csharp
public int LocaleId { get; set; }
```

## Примечания

Список идентификаторов локалей см. по адресу https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Примеры

Показывает, как задать локаль текста, добавляемого с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы установим локаль шрифта на английский язык и вставим русский текст,
// проверка орфографии в английской локали не распознает текст и определит его как орфографическую ошибку.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Установите соответствующую локаль для текста, который мы собираемся добавить, чтобы применить соответствующую проверку орфографии.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
