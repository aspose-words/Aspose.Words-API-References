---
title: Document.Protect
linktitle: Protect
articleTitle: Protect
second_title: Aspose.Words für .NET
description: Schützen Sie Ihre Dokumente mühelos mit Document Protect. Verhindern Sie unbefugte Änderungen, während Sie Ihr bestehendes Passwort beibehalten oder ein zufälliges verwenden.
type: docs
weight: 690
url: /de/net/aspose.words/document/protect/
---
## Protect(*[ProtectionType](../../protectiontype/)*) {#protect}

Schützt das Dokument vor Änderungen, ohne das bestehende Passwort zu ändern oder vergibt ein zufälliges Passwort.

```csharp
public void Protect(ProtectionType type)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| type | ProtectionType | Gibt den Schutztyp für das Dokument an. |

## Bemerkungen

Wenn ein Dokument geschützt ist, kann der Benutzer nur begrenzte Änderungen vornehmen, wie etwa das Hinzufügen von Anmerkungen, das Vornehmen von Überarbeitungen oder das Ausfüllen eines Formulars.

Wenn Sie ein Dokument schützen und das Dokument bereits über ein Schutzkennwort verfügt, wird das vorhandene Schutzkennwort nicht geändert.

Wenn Sie ein Dokument schützen und das Dokument nicht über ein Schutzkennwort verfügt, weist diese Methode ein zufälliges Kennwort zu, das es unmöglich macht, den Schutz des Dokuments in Microsoft Word aufzuheben. Sie können den Schutz des Dokuments in Aspose.Words jedoch trotzdem aufheben, da beim Aufheben des Schutzes kein Kennwort erforderlich ist.

## Beispiele

Zeigt, wie der Schutz für einen Abschnitt deaktiviert wird.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Schreibschutz auf jeden Abschnitt im Dokument anwenden.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Schreibschutz für den ersten Abschnitt deaktivieren.
doc.Sections[0].ProtectedForForms = false;

// In diesem Ausgabedokument können wir den ersten Abschnitt frei bearbeiten,
// und wir können den Inhalt des Formularfelds nur im zweiten Abschnitt bearbeiten.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Siehe auch

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Protect(*[ProtectionType](../../protectiontype/), string*) {#protect_1}

Schützt das Dokument vor Änderungen und legt optional ein Schutzkennwort fest.

```csharp
public void Protect(ProtectionType type, string password)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| type | ProtectionType | Gibt den Schutztyp für das Dokument an. |
| password | String | Das Kennwort, mit dem das Dokument geschützt werden soll. Geben Sie an`null` oder eine leere Zeichenfolge, wenn Sie das Dokument ohne Kennwort schützen möchten. |

## Bemerkungen

Wenn ein Dokument geschützt ist, kann der Benutzer nur begrenzte Änderungen vornehmen, wie etwa das Hinzufügen von Anmerkungen, das Vornehmen von Überarbeitungen oder das Ausfüllen eines Formulars.

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

* enum [ProtectionType](../../protectiontype/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
