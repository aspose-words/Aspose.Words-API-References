---
title: IBibliographyStylesProvider.GetStyle
linktitle: GetStyle
articleTitle: GetStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetStyle-Methode von IBibliographyStylesProvider, um Ihre Bibliografiestile mühelos abzurufen und anzupassen und so Ihr wissenschaftliches Schreiben zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.fields/ibibliographystylesprovider/getstyle/
---
## IBibliographyStylesProvider.GetStyle method

Gibt den Bibliografiestil zurück.

```csharp
public Stream GetStyle(string styleFileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| styleFileName | String | Der Dateiname im Bibliografiestil. |

### Rückgabewert

DerStream mit XSLT-Stylesheet im Bibliografiestil.

## Bemerkungen

Die Implementierung sollte zurückgeben`null` um anzugeben, dass die MS Word-Version des angegebenen Stils verwendet werden soll.

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

* interface [IBibliographyStylesProvider](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
