---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words für .NET
description: LoadOptions Encoding eigendom. Ruft die Kodierung ab die zum Laden eines HTML TXT oder CHMDokuments verwendet wird oder legt diese fest wenn die Kodierung im Dokument nicht angegeben ist . Kann seinNull . Standard istNull  in C#.
type: docs
weight: 50
url: /de/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

Ruft die Kodierung ab, die zum Laden eines HTML-, TXT- oder CHM-Dokuments verwendet wird, oder legt diese fest, wenn die Kodierung im Dokument nicht angegeben ist . Kann sein`Null` . Standard ist`Null` .

```csharp
public Encoding Encoding { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird nur beim Laden von HTML-, TXT- oder CHM-Dokumenten verwendet.

Wenn im Dokument keine Kodierung angegeben ist, diese Eigenschaft jedoch vorhanden ist`Null`dann versucht das System, die Kodierung automatisch zu erkennen.

## Beispiele

Zeigt, wie die Kodierung festgelegt wird, mit der ein Dokument geöffnet wird.

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
