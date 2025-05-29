---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ViewOptions ViewType, позволяющее легко настроить режим просмотра Microsoft Word для повышения производительности и индивидуального редактирования.
type: docs
weight: 40
url: /ru/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Управляет режимом просмотра в Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
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

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* пространство имен [Aspose.Words.Settings](../../../aspose.words.settings/)
* сборка [Aspose.Words](../../../)
