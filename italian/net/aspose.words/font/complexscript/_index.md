---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words per .NET
description: Font ComplexScript proprietà. Specifica se il contenuto di questa esecuzione deve essere trattato come testo di script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione per questa esecuzione in C#.
type: docs
weight: 80
url: /it/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Specifica se il contenuto di questa esecuzione deve essere trattato come testo di script complesso indipendentemente dai valori dei caratteri Unicode quando si determina la formattazione per questa esecuzione.

```csharp
public bool ComplexScript { get; set; }
```

## Esempi

Mostra come aggiungere testo che viene sempre trattato come script complesso.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
