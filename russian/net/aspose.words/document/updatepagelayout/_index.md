---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words для .NET
description: Обновите структуру документа с помощью метода UpdatePageLayout, обеспечивающего безупречный и организованный макет для улучшения читаемости и наглядности.
type: docs
weight: 830
url: /ru/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Перестраивает макет страницы документа.

```csharp
public void UpdatePageLayout()
```

## Примечания

Этот метод форматирует документ на страницы и обновляет поля, связанные с номером страницы в документе such , как PAGE, PAGES, PAGEREF и REF. Актуальная информация о макете страницы необходима для корректного отображения document в форматах с фиксированной страницей.

Этот метод автоматически вызывается, когда вы впервые конвертируете документ в PDF, XPS, изображение или печатаете его. Однако, если вы измените документ после рендеринга, а затем попытаетесь рендерить его снова - Aspose.Words не будет автоматически обновлять макет страницы. В этом случае вам следует вызвать`UpdatePageLayout` before рендеринг снова.

## Примеры

Показывает, когда следует пересчитывать макет страницы документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Сохранение документа в формате PDF, в виде изображения или печать в первый раз автоматически
// кэшируем макет документа на его страницах.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Измените документ каким-либо образом.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// В текущей версии Aspose.Words изменение документа не приводит к его автоматической перестройке
// кэшированный макет страницы. Если мы хотим кэшированный макет
// чтобы оставаться в курсе событий, нам придется обновлять его вручную.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
