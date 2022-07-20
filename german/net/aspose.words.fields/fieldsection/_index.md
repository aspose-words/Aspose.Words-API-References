---
title: FieldSection
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das SECTION-Feld.
type: docs
weight: 2210
url: /de/net/aspose.words.fields/fieldsection/
---
## FieldSection class

Implementiert das SECTION-Feld.

```csharp
public class FieldSection : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldSection](fieldsection)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format) { get; } | erhält a[`FieldFormat`](../fieldformat) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Gibt Text zwischen Feldanfang und Feldtrennzeichen zurück (oder Feldende, wenn kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldergebnis von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Gibt Text zwischen Feldanfang und Feldtrennzeichen (oder Feldende, wenn kein Trennzeichen vorhanden ist) zurück. |
| [Remove](../../aspose.words.fields/field/remove)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Felds das letzte Kind seines Elternknotens ist, wird sein Elternabsatz zurückgegeben. Wenn das Feld bereits entfernt wurde, wird zurückgegeben **Null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Führt das Feld Unlink aus. |
| [Update](../../aspose.words.fields/field/update)() | Führt die Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |
| [Update](../../aspose.words.fields/field/update)(bool) | Führt eine Feldaktualisierung durch. Wird ausgelöst, wenn das Feld bereits aktualisiert wird. |

### Bemerkungen

Ruft die Nummer des aktuellen Abschnitts ab.

### Beispiele

Zeigt, wie die Felder SECTION und SECTIONPAGES verwendet werden, um Seiten nach Abschnitten zu nummerieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;

// Ein SECTION-Feld zeigt die Nummer des Abschnitts an, in dem es sich befindet.
builder.Write("Section ");
FieldSection fieldSection = (FieldSection)builder.InsertField(FieldType.FieldSection, true);

Assert.AreEqual(" SECTION ", fieldSection.GetFieldCode());

// Ein PAGE-Feld zeigt die Nummer der Seite an, auf der es sich befindet.
builder.Write("\nPage ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);

Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// Ein SECTIONPAGES-Feld zeigt die Anzahl der Seiten an, über die sich der Abschnitt erstreckt, in dem es sich befindet.
builder.Write(" of ");
FieldSectionPages fieldSectionPages = (FieldSectionPages)builder.InsertField(FieldType.FieldSectionPages, true);

Assert.AreEqual(" SECTIONPAGES ", fieldSectionPages.GetFieldCode());

// Gehe aus der Kopfzeile zurück in das Hauptdokument und füge zwei Seiten ein.
// Alle diese Seiten befinden sich im ersten Abschnitt. Unsere Felder, die einmal in jedem Header erscheinen,
// nummeriert die aktuellen/gesamten Seiten dieses Abschnitts.
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// So können wir mit dem Document Builder einen neuen Abschnitt einfügen.
// Dies wirkt sich auf die Werte aus, die in den Feldern SECTION und SECTIONPAGES in allen kommenden Kopfzeilen angezeigt werden.
builder.InsertBreak(BreakType.SectionBreakNewPage);

// Das PAGE-Feld zählt die Seiten im gesamten Dokument weiter.
// Wir können die Zählung in jedem Abschnitt manuell zurücksetzen, um die Seiten Abschnitt für Abschnitt zu verfolgen.
builder.CurrentSection.PageSetup.RestartPageNumbering = true;
builder.InsertBreak(BreakType.PageBreak);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SECTION.SECTIONPAGES.docx");
```

### Siehe auch

* class [Field](../field)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
