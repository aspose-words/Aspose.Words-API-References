---
title: IBibliographyStylesProvider Interface
linktitle: IBibliographyStylesProvider
articleTitle: IBibliographyStylesProvider
second_title: Aspose.Words für .NET
description: Aspose.Words.Fields.IBibliographyStylesProvider koppel. Implementieren Sie diese Schnittstelle um den Bibliographiestil für bereitzustellenFieldBibliography UndFieldCitation Felder wenn sie aktualisiert werden in C#.
type: docs
weight: 2670
url: /de/net/aspose.words.fields/ibibliographystylesprovider/
---
## IBibliographyStylesProvider interface

Implementieren Sie diese Schnittstelle, um den Bibliographiestil für bereitzustellen[`FieldBibliography`](../fieldbibliography/) Und[`FieldCitation`](../fieldcitation/) Felder, wenn sie aktualisiert werden.

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
