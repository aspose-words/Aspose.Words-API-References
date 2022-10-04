---
title: FieldStyleRef
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das STYLEREFFeld.
type: docs
weight: 2290
url: /de/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Implementiert das STYLEREF-Feld.

```csharp
public class FieldStyleRef : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldStyleRef](fieldstyleref/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber/) { get; set; } | Ermittelt oder legt fest, ob die Absatznummer des referenzierten Absatzes genau so eingefügt werden soll, wie sie im Dokument erscheint. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext/) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes im vollständigen Kontext eingefügt werden soll. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext/) { get; set; } | Ruft ab oder legt fest, ob die Absatznummer des referenzierten Absatzes in relativen Kontext eingefügt werden soll. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition/) { get; set; } | Ruft ab oder legt fest, ob die relative Position des referenzierten Absatzes eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom/) { get; set; } | Ermittelt oder legt fest, ob auf der aktuellen Seite von unten statt von oben gesucht werden soll. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename/) { get; set; } | Ruft den Namen des Stils ab oder legt ihn fest, nach dem der zu suchende Text formatiert ist. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters/) { get; set; } | Ruft ab oder legt fest, ob Nicht-Trennzeichen unterdrückt werden sollen. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update/)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

STYLEREF wird verwendet, um auf ein Textfragment innerhalb des Dokuments zu verweisen, das mit dem angegebenen Stil formatiert ist.

### Beispiele

Zeigt, wie STYLEREF-Felder verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Liste basierend auf einer Microsoft Word-Listenvorlage.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Diese generierte Liste zeigt "1.a )" an.
 // Das Leerzeichen vor der Klammer ist kein Trennzeichen, das wir unterdrücken können.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Text hinzufügen und Absatzstile anwenden, auf die STYLEREF-Felder verweisen.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Platziere ein STYLEREF-Feld in der Kopfzeile und zeige den ersten Text im "Listenabsatz"-Stil im Dokument an.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Platziere ein STYLEREF-Feld in der Fußzeile und lasse es den letzten Text anzeigen.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Wir können auch STYLEREF-Felder verwenden, um auf die Listennummern von Listen zu verweisen.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
