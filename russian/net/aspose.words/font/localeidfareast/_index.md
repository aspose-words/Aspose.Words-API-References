---
title: Font.LocaleIdFarEast
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает идентификатор локали языка форматированных азиатских символов.
type: docs
weight: 220
url: /ru/net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Получает или задает идентификатор локали (языка) форматированных азиатских символов.

```csharp
public int LocaleIdFarEast { get; set; }
```

### Примечания

Список идентификаторов локали см. на https://msdn.microsoft.com/en-us/library/cc233965.aspx .

### Примеры

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

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


