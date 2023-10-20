---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportTextInputFormFieldAsText eigendom. Steuert wie Texteingabeformularfelder in HTML oder MHTML gespeichert werden. Der Standardwert istFALSCH  in C#.
type: docs
weight: 260
url: /de/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

Steuert, wie Texteingabeformularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## Bemerkungen

Wenn eingestellt auf`WAHR` , exportiert Texteingabeformularfelder als normalen Text. Wann`FALSCH`, exportiert Word-Texteingabeformularfelder als INPUT-Elemente in HTML.

Beim Exportieren nach EPUB werden Texteingabeformularfelder aufgrund der Anforderungen dieses Formats immer als Text gespeichert.

## Beispiele

Zeigt, wie der Ordner zum Speichern verknüpfter Bilder nach dem Speichern im HTML-Format angegeben wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Legen Sie eine Option fest, um Formularfelder als einfachen Text statt als HTML-Eingabeelemente zu exportieren.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
