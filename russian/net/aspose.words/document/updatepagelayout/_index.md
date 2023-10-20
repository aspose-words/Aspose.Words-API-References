---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words для .NET
description: Document UpdatePageLayout метод. Перестраивает макет страницы документа на С#.
type: docs
weight: 770
url: /ru/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Перестраивает макет страницы документа.

```csharp
public void UpdatePageLayout()
```

## Примечания

Этот метод форматирует документ на страницы и обновляет поля, связанные с номером страницы, в документе, такие как PAGE, PAGES, PAGEREF и REF. Актуальная информация о макете страницы необходима для правильного рендеринга document в форматы фиксированных страниц.

Этот метод автоматически вызывается, когда вы впервые конвертируете документ в PDF, XPS, изображение или распечатываете его. Однако, если вы измените документ после рендеринга, а затем попытаетесь отобразить его снова, Aspose.Words не будет обновлять макет страницы автоматически. В этом случае вам следует позвонить`UpdatePageLayout` before рендеринг снова.

## Примеры

Показывает, когда следует пересчитать макет страницы документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Сохранение документа в формате PDF, в изображение или первая печать автоматически
// кэшируем макет документа на его страницах.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Изменить каким-либо образом документ.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // В текущей версии Aspose.Words изменение документа не приводит к автоматической перестройке
// кэшированный макет страницы. Если мы хотим кэшированный макет
// чтобы оставаться в курсе событий, нам нужно будет обновлять его вручную.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
