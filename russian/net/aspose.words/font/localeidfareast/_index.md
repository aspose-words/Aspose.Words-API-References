---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font LocaleIdFarEast, позволяющее легко управлять идентификаторами локали для отформатированных азиатских символов, улучшая тем самым ваши многоязычные приложения.
type: docs
weight: 220
url: /ru/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Возвращает или задает идентификатор локали (язык) форматированных азиатских символов.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Примечания

Список идентификаторов локалей см. по адресу https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Примеры

Показывает, как вставлять и форматировать текст на дальневосточном языке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите настройки шрифта, которые конструктор документов будет применять к любому вставляемому тексту.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Назовите эквиваленты «FarEast» для нашего шрифта и локали.
// Если конструктор вставляет азиатские символы с этой конфигурацией шрифта, то каждый запуск, который содержит
// эти символы будут отображаться с использованием шрифта/локали «FarEast» вместо шрифта/локали по умолчанию.
// Это может быть полезно, когда западный шрифт не имеет идеального представления азиатских символов.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Этот текст будет отображаться с использованием шрифта/локали по умолчанию.
builder.Writeln("Hello world!");

// Поскольку это азиатские символы, в этом запуске будут применены наши эквиваленты шрифта/локали «FarEast».
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
