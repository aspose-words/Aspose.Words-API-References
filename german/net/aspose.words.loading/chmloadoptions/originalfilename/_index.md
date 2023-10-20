---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words für .NET
description: ChmLoadOptions OriginalFileName eigendom. Der Name der CHMDatei. Der Standardwert istNull  in C#.
type: docs
weight: 20
url: /de/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

Der Name der CHM-Datei. Der Standardwert ist`Null` .

```csharp
public string OriginalFileName { get; set; }
```

## Bemerkungen

CHM-Dokumente können Links enthalten, die über den Dateinamen auf dasselbe Dokument verweisen. Aspose.Words unterstützt solche Links und verwendet sie normalerweise[`OriginalFileName`](../../../aspose.words/document/originalfilename/) um zu überprüfen, ob die Datei, auf die ein link verweist, die Datei ist, die geladen wird. Wird ein Dokument aus einem Stream geladen, sollte dessen ursprünglicher Dateiname explizit über diese Eigenschaft angegeben werden, da dieser nicht automatisch ermittelt werden kann.

Wenn ein CHM-Dokument aus einer Datei geladen wird und ein Wert ungleich Null für diese Eigenschaft angegeben wird, hat der Wert Vorrang vor dem tatsächlichen Namen der darin gespeicherten Datei[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Beispiele

Zeigt, wie URLs wie „ms-its:myfile.chm::/index.htm“ aufgelöst werden.

```csharp
// Unser Dokument enthält URLs wie „ms-its:amhelp.chm::....htm“, aber es hat einen anderen Namen,
// Daher funktionieren Dateiverknüpfungen nicht, nachdem sie in HTML gespeichert wurden.
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
