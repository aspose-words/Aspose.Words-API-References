---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words для .NET
description: Откройте для себя свойство BibliographyStyle, с помощью которого можно легко управлять активным стилем вашей библиографии и настраивать его для улучшенной организации и представления.
type: docs
weight: 10
url: /ru/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Возвращает или задает строку, представляющую имя активного стиля для использования в библиографии.

```csharp
public string BibliographyStyle { get; set; }
```

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

* class [Bibliography](../)
* пространство имен [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* сборка [Aspose.Words](../../../)
