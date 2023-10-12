---
title: ImportFormatOptions.IgnoreHeaderFooter
second_title: Aspose.Words per .NET API Reference
description: ImportFormatOptions proprietà. Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito èVERO .
type: docs
weight: 40
url: /it/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto di intestazioni/piè di pagina viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

### Esempi

Mostra come specificare di ignorare o meno la formattazione di origine del contenuto di intestazioni/piè di pagina.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../importformatoptions/)
* assemblea [Aspose.Words](../../../)


