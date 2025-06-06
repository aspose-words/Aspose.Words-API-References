---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: Aspose.Words per .NET
description: Scopri la proprietà KeepLegacyControlChars di OoxmlSaveOptions per mantenere il formato originale dei caratteri di controllo legacy per una conversione fluida dei documenti.
type: docs
weight: 50
url: /it/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Mantiene la rappresentazione originale dei caratteri di controllo legacy.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Esempi

Mostra come supportare i caratteri di controllo legacy durante la conversione in .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Quando salviamo il documento in un formato OOXML, possiamo creare un oggetto OoxmlSaveOptions
// e quindi passarlo al metodo di salvataggio del documento per modificare il modo in cui salviamo il documento.
// Imposta la proprietà "KeepLegacyControlChars" su "true" per preservare
// il carattere legacy "ShortDateTime" durante il salvataggio.
// Imposta la proprietà "KeepLegacyControlChars" su "false" per rimuovere
// il carattere legacy "ShortDateTime" dal documento di output.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Guarda anche

* class [OoxmlSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
