---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words для .NET
description: Улучшите форматирование документов с помощью интерфейса Aspose.Words.IBibliographyStylesProvider, который идеально подходит для настройки стилей библиографии в цитатах.
type: docs
weight: 3080
url: /ru/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Реализуйте этот интерфейс, чтобы обеспечить стиль библиографии для [`FieldBibliography`](../fieldbibliography/) и[`FieldCitation`](../fieldcitation/) поля при их обновлении.

```csharp
public interface IBibliographyStylesProvider
```

## Методы

| Имя | Описание |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Возвращает стиль библиографии. |

## Примеры

Показывает, как переопределить встроенные стили или предоставить пользовательский.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Если у документа уже есть стиль, вы можете изменить его с помощью следующего кода:
    // doc.Bibliography.BibliographyStyle = "Пользовательский стиль библиографии.xsl";

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
