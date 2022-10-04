---
title: FieldAutoNumLgl
second_title: Aspose.Words für .NET-API-Referenz
description: Implementiert das AUTONUMLGLFeld.
type: docs
weight: 1440
url: /de/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

Implementiert das AUTONUMLGL-Feld.

```csharp
public class FieldAutoNumLgl : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | Ruft ab oder legt fest, ob die Zahl ohne nachgestellten Punkt angezeigt werden soll. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | Ruft das zu verwendende Trennzeichen ab oder setzt es. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
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

Fügt eine automatische Nummer im legalen Format ein.

### Beispiele

Zeigt, wie ein Dokument mithilfe von AUTONUMLGL-Feldern organisiert wird.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL-Felder zeigen eine Zahl an, die sich bei jedem AUTONUMLGL-Feld innerhalb der aktuellen Überschriftenebene erhöht.
    // Diese Felder verwalten eine separate Zählung für jede Überschriftenebene,
     // und jedes Feld zeigt auch die Anzahl der AUTONUMLGL-Felder für alle Überschriftenebenen unterhalb seiner eigenen an.
    // Das Ändern der Zählung für eine beliebige Überschriftenebene setzt die Zählungen für alle Ebenen über dieser Ebene auf 1 zurück.
    // Dadurch können wir unser Dokument in Form einer Gliederungsliste organisieren.
    // Dies ist das erste AUTONUMLGL-Feld auf Überschriftenebene 1, das "1" anzeigt. im Dokument.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Dies ist das zweite AUTONUMLGL-Feld auf Überschriftenebene 1, daher wird "2." angezeigt.
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Dies ist das erste AUTONUMLGL-Feld auf Überschriftenebene 2,
    // und der AUTONUMLGL-Zähler für die Überschriftenebene darunter ist "2", also wird "2.1." angezeigt.
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Dies ist das erste AUTONUMLGL-Feld auf Überschriftenebene 3.
    // Auf dieselbe Weise wie im obigen Feld arbeitend, wird "2.1.1." angezeigt.
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Dieses Feld befindet sich auf einer Überschriftenebene von 2 und sein entsprechender AUTONUMLGL-Zähler ist 2, sodass das Feld "2.2." anzeigt.
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Erhöhen des AUTONUMLGL-Zählers für eine Überschriftenebene unterhalb dieser
    // hat die Zählung für dieses Level zurückgesetzt, sodass dieses Feld "2.2.1." anzeigt.
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Das Trennzeichen, das im Feld result unmittelbar nach der Zahl erscheint,
        // ist standardmäßig ein Punkt. Wenn wir diese Eigenschaft null lassen,
        // Unser letztes AUTONUMLGL-Feld zeigt "2.2.1" an. im Dokument.
        Assert.IsNull(field.SeparatorCharacter);

        // Festlegen eines benutzerdefinierten Trennzeichens und Entfernen des nachgestellten Punkts
        // ändert das Aussehen dieses Felds von "2.2.1." zu "2:2:1".
        // Wir wenden dies auf alle Felder an, die wir erstellt haben.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// Verwendet einen Document Builder, um eine Klausel einzufügen, die durch ein AUTONUMLGL-Feld nummeriert ist.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Dieser Text gehört zum Auto-Num-Rechtsfeld darüber.
    // Es wird reduziert, wenn wir auf den Pfeil neben dem entsprechenden AUTONUMLGL-Feld in Microsoft Word klicken.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
