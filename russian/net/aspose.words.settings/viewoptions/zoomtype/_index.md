---
title: ViewOptions.ZoomType
linktitle: ZoomType
articleTitle: ZoomType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ViewOptions ZoomType, позволяющее легко настраивать уровни масштабирования в зависимости от размера окна, что повышает удобство использования и гибкость интерфейса.
type: docs
weight: 60
url: /ru/net/aspose.words.settings/viewoptions/zoomtype/
---
## ViewOptions.ZoomType property

Получает или задает значение масштабирования на основе размера окна.

```csharp
public ZoomType ZoomType { get; set; }
```

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

Показывает, как задать пользовательский тип масштабирования, который старые версии Microsoft Word будут применять к документу при загрузке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Установите свойство "ZoomType" на "ZoomType.PageWidth", чтобы получить Microsoft Word
// для автоматического масштабирования документа по ширине страницы.
// Установите свойство "ZoomType" на "ZoomType.FullPage", чтобы получить Microsoft Word
// для автоматического масштабирования документа, чтобы сделать видимой всю первую страницу.
// Установите свойство "ZoomType" на "ZoomType.TextFit", чтобы получить Microsoft Word
// для автоматического масштабирования документа в соответствии с внутренними текстовыми полями первой страницы.
doc.ViewOptions.ZoomType = zoomType;

doc.Save(ArtifactsDir + "ViewOptions.SetZoomType.doc");
```

### Смотрите также

* enum [ZoomType](../../zoomtype/)
* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
