---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font NameFarEast, которое позволит легко настраивать и задавать названия восточноазиатских шрифтов для улучшения типографики в ваших проектах.
type: docs
weight: 260
url: /ru/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Возвращает или задает имя восточноазиатского шрифта.

```csharp
public string NameFarEast { get; set; }
```

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

* property [Name](../name/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
