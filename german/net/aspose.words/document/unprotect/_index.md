---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words für .NET
description: Document Unprotect methode. Entfernt den Schutz vom Dokument unabhängig vom Passwort in C#.
type: docs
weight: 740
url: /de/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Entfernt den Schutz vom Dokument unabhängig vom Passwort.

```csharp
public void Unprotect()
```

## Bemerkungen

Diese Methode hebt den Schutz des Dokuments auf, selbst wenn es über ein Schutzkennwort verfügt.

Beachten Sie, dass sich der Dokumentschutz vom Schreibschutz unterscheidet. Der Schreibschutz wird mit angegeben[`WriteProtection`](../writeprotection/).

## Beispiele

Zeigt, wie ein Dokument geschützt bzw. der Schutz aufgehoben wird.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Wenn wir dieses Dokument mit Microsoft Word öffnen und es bearbeiten möchten,
// Wir müssen das Passwort anwenden, um den Schutz zu überwinden.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Beachten Sie, dass der Schutz nur für Microsoft Word-Benutzer gilt, die unser Dokument öffnen.
// Wir haben das Dokument in keiner Weise verschlüsselt und benötigen kein Passwort, um es programmgesteuert zu öffnen und zu bearbeiten.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Es gibt zwei Möglichkeiten, den Schutz eines Dokuments aufzuheben.
// 1 - Ohne Passwort:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Mit dem richtigen Passwort:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Unprotect(*string*) {#unprotect}

Entfernt den Schutz vom Dokument, wenn ein korrektes Passwort angegeben wird.

```csharp
public bool Unprotect(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das Passwort, mit dem der Schutz des Dokuments aufgehoben werden soll. |

### Rückgabewert

`WAHR` wenn ein korrektes Passwort angegeben wurde und das Dokument ungeschützt war.

## Bemerkungen

Diese Methode hebt den Schutz des Dokuments nur auf, wenn ein korrektes Passwort angegeben wird.

Beachten Sie, dass sich der Dokumentschutz vom Schreibschutz unterscheidet. Der Schreibschutz wird mit angegeben[`WriteProtection`](../writeprotection/).

## Beispiele

Zeigt, wie ein Dokument geschützt bzw. der Schutz aufgehoben wird.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Wenn wir dieses Dokument mit Microsoft Word öffnen und es bearbeiten möchten,
// Wir müssen das Passwort anwenden, um den Schutz zu überwinden.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Beachten Sie, dass der Schutz nur für Microsoft Word-Benutzer gilt, die unser Dokument öffnen.
// Wir haben das Dokument in keiner Weise verschlüsselt und benötigen kein Passwort, um es programmgesteuert zu öffnen und zu bearbeiten.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Es gibt zwei Möglichkeiten, den Schutz eines Dokuments aufzuheben.
// 1 - Ohne Passwort:
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Mit dem richtigen Passwort:
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
