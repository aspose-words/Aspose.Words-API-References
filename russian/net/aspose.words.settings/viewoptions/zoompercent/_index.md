---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words для .NET
description: ViewOptions ZoomPercent свойство. Получает или задает процент от 10 до 500 с которым вы хотите просмотреть документ на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Получает или задает процент (от 10 до 500), с которым вы хотите просмотреть документ.

```csharp
public int ZoomPercent { get; set; }
```

## Примечания

Если значение равно 0, то это свойство вместо этого использует 100, иначе, если значение меньше 10 или больше 500, это свойство выдает исключение.

Хотя Aspose.Words может читать и записывать эту опцию, ее использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

## Примеры

Показывает, как установить пользовательский коэффициент масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Смотрите также

* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
