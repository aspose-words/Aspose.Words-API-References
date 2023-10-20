---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words per .NET
description: Document Unprotect metodo. Rimuove la protezione dal documento indipendentemente dalla password in C#.
type: docs
weight: 740
url: /it/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Rimuove la protezione dal documento indipendentemente dalla password.

```csharp
public void Unprotect()
```

## Osservazioni

Questo metodo rimuove la protezione del documento anche se dispone di una password di protezione.

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

Rimuove la protezione dal documento se viene specificata una password corretta.

```csharp
public bool Unprotect(string password)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| password | String | La password con cui rimuovere la protezione del documento. |

### Valore di ritorno

`VERO` se è stata specificata una password corretta e il documento non era protetto.

## Osservazioni

Questo metodo rimuove la protezione del documento solo se viene specificata una password corretta.

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

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
