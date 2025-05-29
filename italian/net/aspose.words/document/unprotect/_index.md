---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words per .NET
description: Sblocca senza sforzo i tuoi documenti con il nostro metodo Document Unprotect, rimuovendo qualsiasi protezione tramite password per un facile accesso e modifica.
type: docs
weight: 790
url: /it/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Rimuove la protezione dal documento indipendentemente dalla password.

```csharp
public void Unprotect()
```

## Osservazioni

Questo metodo rimuove la protezione dal documento anche se è stata impostata una password di protezione.

Si noti che la protezione del documento è diversa dalla protezione in scrittura. La protezione in scrittura viene specificata utilizzando[`WriteProtection`](../writeprotection/).

## Esempi

Mostra come proteggere e rimuovere la protezione da un documento.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Se apriamo questo documento con Microsoft Word con l'intenzione di modificarlo,
// dovremo applicare la password per superare la protezione.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Si noti che la protezione si applica solo agli utenti di Microsoft Word che aprono il nostro documento.
// Non abbiamo crittografato il documento in alcun modo e non abbiamo bisogno della password per aprirlo e modificarlo a livello di programmazione.
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
| password | String | Password per rimuovere la protezione dal documento. |

### Valore di ritorno

`VERO`se è stata specificata una password corretta e il documento non era protetto.

## Osservazioni

Questo metodo rimuove la protezione dal documento solo se viene specificata una password corretta.

Si noti che la protezione del documento è diversa dalla protezione in scrittura. La protezione in scrittura viene specificata utilizzando[`WriteProtection`](../writeprotection/).

## Esempi

Mostra come proteggere e rimuovere la protezione da un documento.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Se apriamo questo documento con Microsoft Word con l'intenzione di modificarlo,
// dovremo applicare la password per superare la protezione.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Si noti che la protezione si applica solo agli utenti di Microsoft Word che aprono il nostro documento.
// Non abbiamo crittografato il documento in alcun modo e non abbiamo bisogno della password per aprirlo e modificarlo a livello di programmazione.
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
