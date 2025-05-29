---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup PageHeight, позволяющее эффективно управлять высотой документа в пунктах, улучшая его макет и презентацию.
type: docs
weight: 310
url: /ru/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Возвращает или задает высоту страницы в пунктах.

```csharp
public double PageHeight { get; set; }
```

## Примеры

Показывает, как вставить изображение и использовать его в качестве водяного знака.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте изображение в заголовок, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Разместите изображение в центре страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
