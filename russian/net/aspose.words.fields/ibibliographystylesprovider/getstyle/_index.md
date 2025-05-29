---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words для .NET
description: Откройте для себя метод IBibliographyStylesProvider GetStyle, который позволит вам легко извлекать и настраивать стили библиографии для улучшения академического письма.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Возвращает стиль библиографии.

```csharp
public Stream GetStyle(string styleFileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| styleFileName | String | Имя файла стиля библиографии. |

### Возвращаемое значение

TheStream с таблицей стилей XSLT в стиле библиографии.

## Примечания

Реализация должна вернуть`нулевой` чтобы указать, что следует использовать версию MS Word указанного стиля.

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

* interface [IBibliographyStylesProvider](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
