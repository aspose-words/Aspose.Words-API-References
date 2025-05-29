---
title: FieldOptions.BibliographyStylesProvider
linktitle: BibliographyStylesProvider
articleTitle: BibliographyStylesProvider
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldOptions BibliographyStylesProvider“ für anpassbare Bibliografiestile und verbessern Sie Ihre Felder „FieldBibliography“ und „FieldCitation“.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Ruft einen Provider ab oder legt ihn fest, der einen Bibliographiestil für zurückgibt.[`FieldBibliography`](../../fieldbibliography/) Und[`FieldCitation`](../../fieldcitation/) Felder.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
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

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
