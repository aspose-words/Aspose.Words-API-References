---
title: Document.ProtectionType
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words per .NET
description: Scopri il tipo di protezione attiva dei documenti per una maggiore sicurezza e integrità dei dati. Proteggi i tuoi file senza sforzo con le nostre funzionalità avanzate.
type: docs
weight: 340
url: /it/net/aspose.words/document/protectiontype/
---
## Document.ProtectionType property

Ottiene il tipo di protezione del documento attualmente attivo.

```csharp
public ProtectionType ProtectionType { get; }
```

## Osservazioni

Questa proprietà consente di recuperare il tipo di protezione del documento attualmente impostato. Per modificare il tipo di protezione del documento utilizzare il[`Protect`](../protect/) e[`Unprotect`](../unprotect/) metodi.

Quando un documento è protetto, l'utente può apportare solo modifiche limitate, come aggiungere annotazioni, effettuare revisioni o compilare un modulo.

Si noti che la protezione del documento è diversa dalla protezione in scrittura. La protezione in scrittura viene specificata utilizzando[`WriteProtection`](../writeprotection/)

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
