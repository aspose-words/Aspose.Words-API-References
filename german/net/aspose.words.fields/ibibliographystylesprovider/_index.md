---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words für .NET
description: Verbessern Sie die Formatierung Ihres Dokuments mit der Schnittstelle Aspose.Words.IBibliographyStylesProvider, die sich perfekt zum Anpassen von Bibliografiestilen in Zitaten eignet.
type: docs
weight: 3080
url: /de/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementieren Sie diese Schnittstelle, um einen Bibliographiestil für bereitzustellen.[`FieldBibliography`](../fieldbibliography/) Und[`FieldCitation`](../fieldcitation/) Felder, wenn sie aktualisiert werden.

```csharp
public interface IBibliographyStylesProvider
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetStyle](../../aspose.words.fields/ibibliographystylesprovider/getstyle/)(*string*) | Gibt den Bibliografiestil zurück. |

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

* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
