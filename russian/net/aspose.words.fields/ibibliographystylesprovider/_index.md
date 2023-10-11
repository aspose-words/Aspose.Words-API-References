---
title: Interface IBibliographyStylesProvider
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider интерфейс. Реализуйте этот интерфейс чтобы обеспечить стиль библиографии для FieldBibliography иFieldCitation поля когда они обновляются.
type: docs
weight: 2670
url: /ru/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Реализуйте этот интерфейс, чтобы обеспечить стиль библиографии для [`FieldBibliography`](../fieldbibliography/) и[`FieldCitation`](../fieldcitation/) поля, когда они обновляются.

```csharp
public interface IBibliographyStylesProvider
```

## Методы

| Имя | Описание |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(string) | Возвращает стиль библиографии. |

### Примеры

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


