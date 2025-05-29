---
title: ViewOptions.ZoomPercent
linktitle: ZoomPercent
articleTitle: ZoomPercent
second_title: Aspose.Words для .NET
description: Настройте свойство ViewOptions ZoomPercent, чтобы задать уровень масштабирования документа в диапазоне от 10 до 500%. Улучшите читаемость и оптимизируйте процесс просмотра!
type: docs
weight: 50
url: /ru/net/aspose.words.settings/viewoptions/zoompercent/
---
## ViewOptions.ZoomPercent property

Возвращает или задает процент, с которым вы хотите просматривать документ.

```csharp
public int ZoomPercent { get; set; }
```

## Примечания

Хотя Aspose.Words может читать и записывать этот параметр, его использование зависит от приложения. Например, MS Word 2013 не учитывает значение этого параметра.

## Примеры

Показывает, как задать пользовательский коэффициент масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

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
