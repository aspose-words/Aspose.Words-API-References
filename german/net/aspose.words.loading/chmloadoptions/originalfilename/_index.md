---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChmLoadOptions OriginalFileName-Eigenschaft und legen Sie den CHM-Dateinamen für einen optimierten Zugriff einfach fest. Der Standardwert ist null. Optimieren Sie Ihr Erlebnis!
type: docs
weight: 20
url: /de/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Der Name der CHM-Datei. Der Standardwert ist`null` .

```csharp
public string OriginalFileName { get; set; }
```

## Bemerkungen

CHM-Dokumente können Links enthalten, die über den Dateinamen auf dasselbe Dokument verweisen. Aspose.Words unterstützt solche Links und verwendet normalerweise[`OriginalFileName`](../../../aspose.words/document/originalfilename/) um zu prüfen, ob die durch einen Link referenzierte Datei die geladene Datei ist. Wird ein Dokument aus einem Stream geladen, sollte der ursprüngliche Dateiname explizit über diese Eigenschaft angegeben werden, da er nicht automatisch ermittelt werden kann.

Wenn ein CHM-Dokument aus einer Datei geladen wird und ein Wert ungleich Null für diese Eigenschaft angegeben wird, hat der Wert Vorrang vor dem tatsächlichen Namen der Datei, die in[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Beispiele

Zeigt, wie URLs wie „ms-its:myfile.chm::/index.htm“ aufgelöst werden.

```csharp
// Unser Dokument enthält URLs wie "ms-its:amhelp.chm::....htm", hat aber einen anderen Namen,
// daher funktionieren Dateilinks nach dem Speichern im HTML-Format nicht.
// Wir müssen den ursprünglichen Dateinamen in „ChmLoadOptions“ definieren, um dieses Verhalten zu vermeiden.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Siehe auch

* class [ChmLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
