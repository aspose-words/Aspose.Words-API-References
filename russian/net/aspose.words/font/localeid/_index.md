---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words для .NET
description: Font LocaleId свойство. Получает или задает идентификатор локали языка форматированных символов на С#.
type: docs
weight: 200
url: /ru/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Получает или задает идентификатор локали (языка) форматированных символов.

```csharp
public int LocaleId { get; set; }
```

## Примечания

Список идентификаторов локали см. на https://msdn.microsoft.com/en-us/library/cc233965.aspx .

## Примеры

Показывает, как установить языковой стандарт текста, который мы добавляем с помощью построителя документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если мы установим английский язык шрифта и вставим русский текст,
// программа проверки правописания английской локали не распознает текст и обнаружит в нем орфографическую ошибку.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Установите соответствующий локаль для текста, который мы собираемся добавить, чтобы применить соответствующую проверку орфографии.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
