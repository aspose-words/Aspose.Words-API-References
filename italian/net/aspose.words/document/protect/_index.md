---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words per .NET
description: Document Protect metodo. Protegge il documento da modifiche senza cambiare la password esistente o assegna una password casuale in C#.
type: docs
weight: 650
url: /it/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Protegge il documento da modifiche senza cambiare la password esistente o assegna una password casuale.

```csharp
public void Protect(ProtectionType type)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| type | ProtectionType | Specifica il tipo di protezione per il documento. |

## Osservazioni

Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, apportare revisioni o completare un modulo.

Quando proteggi un documento e il documento ha già una password di protezione, la password di protezione esistente non viene modificata.

Quando proteggi un documento e il documento non ha una password di protezione, questo metodo assegna una password casuale che rende impossibile rimuovere la protezione del documento in Microsoft Word, ma puoi comunque rimuovere la protezione del documento in Aspose.Words poiché non richiedere una password quando si rimuove la protezione.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Protegge il documento dalle modifiche e facoltativamente imposta una password di protezione.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| type | ProtectionType | Specifica il tipo di protezione per il documento. |
| password | String | La password con cui proteggere il documento. Specificare`nullo`oppure una stringa vuota se si desidera proteggere il documento senza password. |

## Osservazioni

Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, apportare revisioni o completare un modulo.

Tieni presente che la protezione del documento è diversa dalla protezione da scrittura. La protezione da scrittura viene specificata utilizzando il file[`WriteProtection`](../writeprotection/).

## Esempi

Mostra come proteggere e rimuovere la protezione di un documento.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Se apriamo questo documento con Microsoft Word con l'intenzione di modificarlo,
// dovremo applicare la password per superare la protezione.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Tieni presente che la protezione si applica solo agli utenti di Microsoft Word che aprono il nostro documento.
// Non abbiamo crittografato il documento in alcun modo e non abbiamo bisogno della password per aprirlo e modificarlo a livello di codice.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Esistono due modi per rimuovere la protezione da un documento.
// 1 - Senza password:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Con la password corretta:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Guarda anche

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
