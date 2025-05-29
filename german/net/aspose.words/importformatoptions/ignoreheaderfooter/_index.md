---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImportFormatOptions IgnoreHeaderFooter-Eigenschaft und steuern Sie die Kopf-/Fußzeilenformatierung im KeepSourceFormatting-Modus. Vereinfachen Sie noch heute Ihren Dokumentimport!
type: docs
weight: 40
url: /de/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass die Quellformatierung von Kopf-/Fußzeileninhalten ignoriert wird , wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Beispiele

Zeigt, wie die Quellformatierung von Kopf-/Fußzeileninhalten ignoriert werden soll oder nicht.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Wenn 'IgnoreHeaderFooter' falsch ist, dann wird die ursprüngliche Formatierung für Kopf-/Fußzeileninhalte
// aus "Header and footer types.docx" wird verwendet.
// Wenn 'IgnoreHeaderFooter' wahr ist, dann die Formatierung für Kopf-/Fußzeileninhalte
// aus "Document.docx" wird verwendet.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
