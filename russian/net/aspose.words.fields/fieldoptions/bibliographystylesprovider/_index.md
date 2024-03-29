---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words для .NET
description: FieldOptions BibliographyStylesProvider свойство. Получает или задает поставщика который возвращает стиль библиографии для FieldBibliography иFieldCitation поля на С#.
type: docs
weight: 20
url: /ru/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Получает или задает поставщика, который возвращает стиль библиографии для [`FieldBibliography`](../../fieldbibliography/) и[`FieldCitation`](../../fieldcitation/) поля.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

## Примеры

Показывает, как переопределить встроенные стили или использовать собственные.

```csharp
public void ChangeBibliographyStyles()
{            
    Document doc = new Document(MyDir + "Bibliography.docx");

    doc.FieldOptions.BibliographyStylesProvider = new BibliographyStylesProvider();
    doc.UpdateFields();

    doc.Save(ArtifactsDir + "Field.ChangeBibliographyStyles.docx");
}

public class BibliographyStylesProvider : IBibliographyStylesProvider
{
    Stream IBibliographyStylesProvider.GetStyle(string styleFileName)
    {
        return File.OpenRead(MyDir + "Bibliography custom style.xsl");
    }
}
```

### Смотрите также

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
