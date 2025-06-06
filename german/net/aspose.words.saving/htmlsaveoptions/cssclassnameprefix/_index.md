---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „HtmlSaveOptions CssClassNamePrefix“, um CSS-Klassennamen einfach mit einem eindeutigen Präfix anzupassen und so die Konsistenz Ihres Webdesigns zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Gibt ein Präfix an, das allen CSS-Klassennamen hinzugefügt wird. Der Standardwert ist eine leere Zeichenfolge und generierte CSS-Klassennamen haben kein gemeinsames Präfix.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentException | Der Wert ist nicht leer und kein gültiger CSS-Bezeichner. |

## Bemerkungen

Wenn dieser Wert nicht leer ist, beginnen alle von Aspose.Words generierten CSS-Klassen mit dem angegebenen Präfix. . Dies kann beispielsweise nützlich sein, wenn Sie generierten Dokumenten benutzerdefiniertes CSS hinzufügen und Namenskonflikte der Klasse vermeiden möchten.

Wenn der Wert nicht`null` oder leer, es muss ein gültiger CSS-Bezeichner sein.

## Beispiele

Zeigt, wie Sie ein Dokument im HTML-Format speichern und allen CSS-Klassennamen ein Präfix hinzufügen.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
