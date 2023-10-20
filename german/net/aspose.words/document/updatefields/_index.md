---
title: Document.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words für .NET
description: Document UpdateFields methode. Aktualisiert die Werte von Feldern im gesamten Dokument in C#.
type: docs
weight: 750
url: /de/net/aspose.words/document/updatefields/
---
## Document.UpdateFields method

Aktualisiert die Werte von Feldern im gesamten Dokument.

```csharp
public void UpdateFields()
```

## Bemerkungen

Wenn Sie ein Dokument öffnen, ändern und dann speichern, aktualisiert Aspose.Words die Felder nicht automatisch, sondern behält sie intakt. Daher möchten Sie diese Methode normalerweise vor dem Speichern aufrufen, wenn Sie das Dokument programmgesteuert geändert haben und dies sicherstellen möchten Die richtigen (berechneten) Feldwerte werden im gespeicherten Dokument angezeigt.

Es besteht keine Notwendigkeit, Felder nach der Ausführung eines Serienbriefs zu aktualisieren, da der Serienbrief eine Art Feldaktualisierung ist und automatisch alle Felder im Dokument aktualisiert.

Diese Methode aktualisiert nicht alle Feldtypen. Eine detaillierte Liste der unterstützten Feldtypen finden Sie im Programmierhandbuch.

Diese Methode aktualisiert keine Felder, die sich auf die Seitenlayout-Algorithmen beziehen (z. B. PAGE, PAGES, PAGEREF). Die seitenlayoutbezogenen Felder werden aktualisiert, wenn Sie ein Dokument oder einen Aufruf rendern[`UpdatePageLayout`](../updatepagelayout/).

Benutzen Sie die[`NormalizeFieldTypes`](../normalizefieldtypes/) Methode vor der Aktualisierung von Feldern, wenn es Dokumentänderungen gab, die sich auf Feldtypen auswirkten.

Um Felder in einem bestimmten Teil des Dokuments zu aktualisieren, verwenden Sie[`UpdateFields`](../../range/updatefields/).

## Beispiele

Zeigt die Verwendung des QUOTE-Felds an.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein QUOTE-Feld einfügen, das den Wert seiner Text-Eigenschaft anzeigt.
FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
field.Text = "\"Quoted text\"";

Assert.AreEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.GetFieldCode());

// Ein QUOTE-Feld einfügen und darin ein DATE-Feld verschachteln.
// DATE-Felder aktualisieren ihren Wert jedes Mal auf das aktuelle Datum, wenn wir das Dokument mit Microsoft Word öffnen.
// Wenn Sie das DATE-Feld auf diese Weise im QUOTE-Feld verschachteln, wird dessen Wert eingefroren
// bis zum Datum, an dem wir das Dokument erstellt haben.
builder.Write("\nDocument creation date: ");
field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
builder.MoveTo(field.Separator);
builder.InsertField(FieldType.FieldDate, true);

Assert.AreEqual(" QUOTE \u0013 DATE \u0014" + DateTime.Now.Date.ToShortDateString() + "\u0015", field.GetFieldCode());

// Alle Felder aktualisieren, um die korrekten Ergebnisse anzuzeigen.
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
 // die jeweiligen Eigenschaften des UserInformation-Objekts, das wir oben erstellt haben.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// Das Feldoptionsobjekt verfügt außerdem über einen statischen Standardbenutzer, auf den Felder aus allen Dokumenten verweisen können.
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

Zeigt, wie man ein Inhaltsverzeichnis (TOC) in ein Dokument einfügt, indem man Überschriftenstile als Einträge verwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis für die erste Seite des Dokuments einfügen.
// Konfigurieren Sie die Tabelle so, dass sie Absätze mit Überschriften der Ebenen 1 bis 3 aufnimmt.
// Legen Sie außerdem fest, dass seine Einträge Hyperlinks sind, die uns weiterleiten
// zur Position der Überschrift, wenn in Microsoft Word mit der linken Maustaste darauf geklickt wird.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
