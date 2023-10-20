---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words для .NET
description: Font NameFarEast свойство. Возвращает или задает имя восточноазиатского шрифта на С#.
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

// Укажите настройки шрифта, которые построитель документов будет применять к любому вставляемому тексту.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Назовите «Дальневосточные» эквиваленты нашего шрифта и локали.
// Если сборщик вставляет азиатские символы с этой конфигурацией шрифта, то каждый запуск, содержащий
// эти символы будут отображаться с использованием шрифта/локали «Fareast» вместо значения по умолчанию.
// Это может быть полезно, если западный шрифт не имеет идеального представления азиатских символов.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Этот текст будет отображаться в шрифте/локали по умолчанию.
builder.Writeln("Hello world!");

// Поскольку это азиатские символы, при этом будут применены эквиваленты нашего шрифта/локали «Дальнего Востока».
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Смотрите также

* property [Name](../name/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
