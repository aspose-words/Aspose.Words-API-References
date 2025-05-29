---
title: Document.ViewOptions
linktitle: ViewOptions
articleTitle: ViewOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Document ViewOptions, чтобы настроить параметры отображения Microsoft Word для индивидуального просмотра.
type: docs
weight: 490
url: /ru/net/aspose.words/document/viewoptions/
---
## Document.ViewOptions property

Предоставляет параметры для управления отображением документа в Microsoft Word.

```csharp
public ViewOptions ViewOptions { get; }
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

* class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
