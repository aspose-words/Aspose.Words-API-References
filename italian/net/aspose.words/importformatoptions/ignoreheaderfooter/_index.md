---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words per .NET
description: Scopri la proprietà IgnoreHeaderFooter di ImportFormatOptions e controlla la formattazione di intestazioni/piè di pagina in modalità KeepSourceFormatting. Semplifica l'importazione dei tuoi documenti oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle intestazioni/piè di pagina viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Esempi

Mostra come specificare se ignorare o meno la formattazione originale del contenuto di intestazioni/piè di pagina.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Se 'IgnoreHeaderFooter' è falso, la formattazione originale per il contenuto dell'intestazione/piè di pagina
// Verrà utilizzato "Tipi di intestazione e piè di pagina.docx".
// Se 'IgnoreHeaderFooter' è vero, la formattazione per il contenuto dell'intestazione/piè di pagina
// da "Document.docx" verrà utilizzato.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
