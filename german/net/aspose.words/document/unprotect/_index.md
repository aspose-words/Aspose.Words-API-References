---
title: Document.Unprotect
linktitle: Unprotect
articleTitle: Unprotect
second_title: Aspose.Words für .NET
description: Entsperren Sie Ihre Dokumente mühelos mit unserer Methode zum Aufheben des Dokumentschutzes und entfernen Sie jeglichen Kennwortschutz für einfachen Zugriff und einfache Bearbeitung.
type: docs
weight: 790
url: /de/net/aspose.words/document/unprotect/
---
## Unprotect() {#unprotect_1}

Entfernt den Schutz des Dokuments, unabhängig vom Kennwort.

```csharp
public void Unprotect()
```

## Bemerkungen

Mit dieser Methode wird der Dokumentschutz aufgehoben, auch wenn das Dokument mit einem Kennwort geschützt ist.

Beachten Sie, dass sich der Dokumentenschutz vom Schreibschutz unterscheidet. Der Schreibschutz wird mithilfe des[`WriteProtection`](../writeprotection/).

## Beispiele

Zeigt, wie Sie ein Dokument schützen und den Schutz aufheben.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Wenn wir dieses Dokument mit Microsoft Word öffnen, um es zu bearbeiten,
// Wir müssen das Passwort anwenden, um den Schutz zu umgehen.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Beachten Sie, dass der Schutz nur für Microsoft Word-Benutzer gilt, die unser Dokument öffnen.
// Wir haben das Dokument in keiner Weise verschlüsselt und benötigen das Kennwort nicht, um es programmgesteuert zu öffnen und zu bearbeiten.
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

Entfernt den Schutz vom Dokument, wenn ein korrektes Kennwort angegeben ist.

```csharp
public bool Unprotect(string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| password | String | Das Kennwort, mit dem der Dokumentschutz aufgehoben werden soll. |

### Rückgabewert

`WAHR`wenn ein korrektes Passwort angegeben wurde und das Dokument ungeschützt war.

## Bemerkungen

Diese Methode hebt den Dokumentschutz nur auf, wenn ein korrektes Kennwort angegeben wird.

Beachten Sie, dass sich der Dokumentenschutz vom Schreibschutz unterscheidet. Der Schreibschutz wird mithilfe des[`WriteProtection`](../writeprotection/).

## Beispiele

Zeigt, wie Sie ein Dokument schützen und den Schutz aufheben.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Wenn wir dieses Dokument mit Microsoft Word öffnen, um es zu bearbeiten,
// Wir müssen das Passwort anwenden, um den Schutz zu umgehen.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Beachten Sie, dass der Schutz nur für Microsoft Word-Benutzer gilt, die unser Dokument öffnen.
// Wir haben das Dokument in keiner Weise verschlüsselt und benötigen das Kennwort nicht, um es programmgesteuert zu öffnen und zu bearbeiten.
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
