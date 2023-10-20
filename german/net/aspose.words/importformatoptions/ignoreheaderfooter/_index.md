---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words für .NET
description: ImportFormatOptions IgnoreHeaderFooter eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt dass die Quellformatierung des Kopf/Fußzeileninhalts ignoriert wird wennKeepSourceFormatting Modus wird verwendet. Der Standardwert istWAHR  in C#.
type: docs
weight: 40
url: /de/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, dass die Quellformatierung des Kopf-/Fußzeileninhalts ignoriert wird wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Beispiele

Zeigt, wie festgelegt wird, ob die Quellformatierung des Kopf-/Fußzeileninhalts ignoriert oder nicht formatiert werden soll.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
