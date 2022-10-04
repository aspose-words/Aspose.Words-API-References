---
title: UpdateFields
second_title: Aspose.Words für .NET-API-Referenz
description: Aktualisiert die Werte von Feldern im gesamten Dokument.
type: docs
weight: 730
url: /de/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Aktualisiert die Werte von Feldern im gesamten Dokument.

```csharp
public void UpdateFields()
```

### Bemerkungen

Wenn Sie ein Dokument öffnen, ändern und dann speichern, aktualisiert Aspose.Words Felder nicht automatisch, sondern behält sie bei. Daher sollten Sie diese Methode normalerweise vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und sicherstellen möchten die richtigen (berechneten) Feldwerte erscheinen im gespeicherten Dokument.

Es ist nicht erforderlich, Felder nach dem Ausführen eines Seriendrucks zu aktualisieren, da der Seriendruck eine Art Feldaktualisierung ist und automatisch alle Felder im Dokument aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Eine detaillierte Liste der unterstützten Feldtypen finden Sie im Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die sich auf die Seitenlayout-Algorithmen beziehen (z. B. PAGE, PAGES, PAGEREF). Die Seitenlayout-bezogenen Felder werden aktualisiert, wenn Sie ein Dokument rendern oder aufrufen[`UpdatePageLayout`](../updatepagelayout/).

Verwenden Sie die[`NormalizeFieldTypes`](../normalizefieldtypes/) -Methode vor der Feldaktualisierung, wenn es Dokumentänderungen gab, die sich auf Feldtypen auswirkten.

Verwenden Sie zum Aktualisieren von Feldern in einem bestimmten Teil des Dokuments[`UpdateFields`](../../range/updatefields/).

### Beispiele

Zeigt die Verwendung des QUOTE-Felds an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Füge ein QUOTE-Feld ein, das den Wert seiner Text-Eigenschaft anzeigt.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Ein QUOTE-Feld einfügen und ein DATE-Feld darin verschachteln.
// DATE-Felder aktualisieren ihren Wert jedes Mal auf das aktuelle Datum, wenn wir das Dokument mit Microsoft Word öffnen.
// Wenn Sie das DATE-Feld so in das QUOTE-Feld verschachteln, wird sein Wert eingefroren
// bis zu dem Datum, an dem wir das Dokument erstellt haben.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Aktualisieren Sie alle Felder, um ihre korrekten Ergebnisse anzuzeigen.
doc.UpdateFields();

Assert.AreEqual("\"Quoted text\"", doc.Range.Fields[0].Result);

doc.Save(ArtifactsDir + "Field.QUOTE.docx");
```

Zeigt, wie Benutzerdetails festgelegt und mithilfe von Feldern angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein UserInformation-Objekt und legen Sie es als Datenquelle für Felder fest, die Benutzerinformationen anzeigen.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Felder USERNAME, USERINITIALS und USERADDRESS einfügen, die Werte von anzeigen
// die entsprechenden Eigenschaften des oben erstellten UserInformation-Objekts. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Das Feldoptionsobjekt hat auch einen statischen Standardbenutzer, auf den sich Felder aus allen Dokumenten beziehen können.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

Zeigt, wie Sie ein Inhaltsverzeichnis (TOC) in ein Dokument einfügen, indem Sie Überschriftenstile als Einträge verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis für die erste Seite des Dokuments einfügen.
// Konfigurieren Sie die Tabelle, um Absätze mit Überschriften der Ebenen 1 bis 3 aufzunehmen.
// Legen Sie außerdem seine Einträge als Hyperlinks fest, die uns führen
// an die Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste geklickt wird.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftenstilen hinzufügen.
// Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erstellt einen Eintrag in der Tabelle.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Ein Inhaltsverzeichnis ist ein Feld eines Typs, der aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
