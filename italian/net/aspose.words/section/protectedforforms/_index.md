---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words per .NET
description: Section ProtectedForForms proprietà. Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word in C#.
type: docs
weight: 60
url: /it/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli, gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

## Esempi

Mostra come disattivare la protezione per una sezione.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Applica la protezione da scrittura a ogni sezione del documento.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Disattiva la protezione da scrittura per la prima sezione.
doc.Sections[0].ProtectedForForms = false;

// In questo documento di output, potremo modificare liberamente la prima sezione,
// e potremo modificare solo il contenuto del campo del modulo nella seconda sezione.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
