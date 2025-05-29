---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words für .NET
description: Entdecken Sie die LoadOptions-Kodierungseigenschaft, um die Kodierung von HTML-, TXT- oder CHM-Dokumenten einfach zu verwalten. Passen Sie das Laden Ihrer Inhalte für optimale Leistung an!
type: docs
weight: 50
url: /de/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ruft die Kodierung ab oder legt sie fest, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`null` Standard ist`null` .

```csharp
public Encoding Encoding { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn die Kodierung im Dokument nicht angegeben ist und diese Eigenschaft`null`dann versucht das System, die Kodierung automatisch zu erkennen.

## Beispiele

Zeigt, wie die Kodierung zum Öffnen eines Dokuments festgelegt wird.

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// Laden Sie das Dokument, während Sie das LoadOptions-Objekt übergeben, und überprüfen Sie dann den Inhalt des Dokuments.
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
