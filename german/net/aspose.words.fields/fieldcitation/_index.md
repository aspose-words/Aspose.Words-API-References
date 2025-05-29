---
title: FieldCitation Class
linktitle: FieldCitation
articleTitle: FieldCitation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldCitation für nahtloses Zitationsmanagement in Dokumenten. Verbessern Sie Ihre Texte mit effizienter Feldimplementierung!
type: docs
weight: 2090
url: /de/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Implementiert das Feld CITATION.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldCitation : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldCitation](fieldcitation/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der dem**Etikett** Elementwert einer anderen Quelle, der in das Zitat aufgenommen werden soll. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid/) { get; set; } | Ruft die Sprachkennung ab oder legt sie fest, die in Verbindung mit dem angegebenen bibliografischen Stil zum Formatieren des Zitats im Dokument verwendet wird. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber/) { get; set; } | Ruft eine mit dem Zitat verknüpfte Seitenzahl ab oder legt sie fest. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix/) { get; set; } | Ruft ein Präfix ab oder legt es fest, das dem Zitat vorangestellt wird. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der dem**Etikett** Elementwert der einzufügenden Quelle. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix/) { get; set; } | Ruft ein Suffix ab oder legt es fest, das an das Zitat angehängt wird. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor/) { get; set; } | Ruft ab oder legt fest, ob die Autoreninformationen aus dem Zitat unterdrückt werden. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle/) { get; set; } | Ruft ab oder legt fest, ob die Titelinformationen aus dem Zitat unterdrückt werden. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear/) { get; set; } | Ruft ab oder legt fest, ob die Jahresangabe aus dem Zitat unterdrückt wird. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber/) { get; set; } | Ruft eine mit dem Zitat verknüpfte Bandnummer ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern werden einbezogen. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines übergeordneten Knotens ist, wird dessen übergeordneter Absatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt die Feldverknüpfung aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

## Bemerkungen

Fügt den Inhalt der**Quelle** Element mit einem angegebenen**Etikett** Element im bibliografischen Stil.

## Beispiele

Zeigt, wie mit den Feldern CITATION und BIBLIOGRAPHY gearbeitet wird.

```csharp
// Öffnen Sie ein Dokument mit bibliographischen Quellen, die wir finden können in
// Microsoft Word über Verweise -> Zitate & Bibliografie -> Quellen verwalten.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Erstellen Sie ein Zitat nur mit der Seitenzahl und dem Autor des referenzierten Buches.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Wir verweisen auf Quellen anhand ihrer Tag-Namen.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Erstellen Sie ein ausführlicheres Zitat, das zwei Quellen zitiert.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Wir können ein BIBLIOGRAPHY-Feld verwenden, um alle Quellen im Dokument anzuzeigen.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
