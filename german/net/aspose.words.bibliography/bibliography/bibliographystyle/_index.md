---
title: Bibliography.BibliographyStyle
linktitle: BibliographyStyle
articleTitle: BibliographyStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die BibliographyStyle-Eigenschaft, mit der Sie den aktiven Stil Ihrer Bibliografie ganz einfach verwalten und anpassen können, um eine bessere Organisation und Präsentation zu erzielen.
type: docs
weight: 10
url: /de/net/aspose.words.bibliography/bibliography/bibliographystyle/
---
## Bibliography.BibliographyStyle property

Ruft eine Zeichenfolge ab oder legt sie fest, die den Namen des aktiven Stils darstellt, der für eine Bibliografie verwendet werden soll.

```csharp
public string BibliographyStyle { get; set; }
```

## Beispiele

Zeigt, wie integrierte Stile überschrieben oder benutzerdefinierte Stile bereitgestellt werden.

```csharp
public void ChangeBibliographyStyles()
{
    Document doc = new Document(MyDir + "Bibliography.docx");

    // Wenn das Dokument bereits einen Stil hat, können Sie ihn mit dem folgenden Code ändern:
    // doc.Bibliography.BibliographyStyle = "Bibliography benutzerdefinierter Stil.xsl";

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

### Siehe auch

* class [Bibliography](../)
* namensraum [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../../)
