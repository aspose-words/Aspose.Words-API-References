---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ProtectionType per una solida sicurezza dei documenti. Migliora i tuoi documenti con opzioni di protezione personalizzabili oggi stesso!
type: docs
weight: 5240
url: /it/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Tipo di protezione per un documento.

```csharp
public enum ProtectionType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AllowOnlyComments | `1` | L'utente può modificare solo i commenti nel documento. |
| AllowOnlyFormFields | `2` | L'utente può inserire dati solo nei campi del modulo nel documento. |
| AllowOnlyRevisions | `0` | L'utente può solo aggiungere segni di revisione al documento. |
| ReadOnly | `3` | Non sono consentite modifiche al documento. Disponibile da Microsoft Word 2003. |
| NoProtection | `-1` | Il documento non è protetto. |

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
// e potremo modificare il contenuto del campo del modulo solo nella seconda sezione.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
