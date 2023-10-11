---
title: FieldOptions.BibliographyStylesProvider
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft einen Anbieter ab oder legt ihn fest der einen Bibliografiestil für zurückgibtFieldBibliography UndFieldCitation Felder.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldoptions/bibliographystylesprovider/
---
## FieldOptions.BibliographyStylesProvider property

Ruft einen Anbieter ab oder legt ihn fest, der einen Bibliografiestil für zurückgibt[`FieldBibliography`](../../fieldbibliography/) Und[`FieldCitation`](../../fieldcitation/) Felder.

```csharp
public IBibliographyStylesProvider BibliographyStylesProvider { get; set; }
```

### Beispiele

Zeigt, wie integrierte Stile überschrieben oder benutzerdefinierte Stile bereitgestellt werden.

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

### Siehe auch

* interface [IBibliographyStylesProvider](../../ibibliographystylesprovider/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


