---
title: FieldAutoNumLgl Class
linktitle: FieldAutoNumLgl
articleTitle: FieldAutoNumLgl
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.FieldAutoNumLgl für die nahtlose Implementierung von AUTONUMLGL-Feldern und verbessern Sie die Dokumentautomatisierung und -formatierung.
type: docs
weight: 2000
url: /de/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

Implementiert das AUTONUMLGL-Feld.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod/) { get; set; } | Ruft ab oder legt fest, ob die Zahl ohne abschließenden Punkt angezeigt werden soll. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter/) { get; set; } | Ruft das zu verwendende Trennzeichen ab oder legt es fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |

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

Fügt eine automatische Nummer im legalen Format ein.

## Beispiele

Zeigt, wie ein Dokument mithilfe von AUTONUMLGL-Feldern organisiert wird.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL-Felder zeigen eine Zahl an, die bei jedem AUTONUMLGL-Feld innerhalb der aktuellen Überschriftenebene erhöht wird.
    // Diese Felder verwalten eine separate Zählung für jede Überschriftenebene,
        // und jedes Feld zeigt auch die AUTONUMLGL-Feldanzahl für alle Überschriftenebenen unter seiner eigenen an.
    // Wenn Sie die Anzahl für eine Überschriftenebene ändern, werden die Anzahlen für alle Ebenen über dieser Ebene auf 1 zurückgesetzt.
    // Dadurch können wir unser Dokument in Form einer Gliederungsliste organisieren.
    // Dies ist das erste AUTONUMLGL-Feld auf der Überschriftenebene 1, das im Dokument „1.“ anzeigt.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Dies ist das zweite AUTONUMLGL-Feld auf der Überschriftenebene 1 und zeigt daher „2.“ an.
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Dies ist das erste AUTONUMLGL-Feld auf Überschriftenebene 2,
    // und der AUTONUMLGL-Zähler für die Überschriftenebene darunter ist „2“, daher wird „2.1.“ angezeigt.
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

        // Dies ist das erste AUTONUMLGL-Feld auf Überschriftenebene 3.
    // Funktioniert auf die gleiche Weise wie das Feld oben, zeigt aber „2.1.1.“ an.
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Dieses Feld befindet sich auf der Überschriftenebene 2 und sein entsprechender AUTONUMLGL-Zähler beträgt 2, daher wird im Feld „2.2.“ angezeigt.
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Inkrementieren des AUTONUMLGL-Zählers für eine Überschriftenebene unterhalb dieser
    // hat den Zähler für diese Ebene zurückgesetzt, sodass in diesem Feld „2.2.1.“ angezeigt wird.
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Das Trennzeichen, das im Feldergebnis unmittelbar nach der Zahl erscheint,
        // ist standardmäßig ein Punkt. Wenn wir diese Eigenschaft null lassen,
        // Unser letztes AUTONUMLGL-Feld zeigt im Dokument „2.2.1.“ an.
        Assert.IsNull(field.SeparatorCharacter);

        // Festlegen eines benutzerdefinierten Trennzeichens und Entfernen des abschließenden Punkts
        // ändert das Erscheinungsbild dieses Feldes von „2.2.1.“ in „2:2:1“.
        // Wir werden dies auf alle Felder anwenden, die wir erstellt haben.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Verwendet einen Dokumentgenerator, um eine durch ein AUTONUMLGL-Feld nummerierte Klausel einzufügen.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Dieser Text gehört zum darüber liegenden Autonum-Rechtsfeld.
    // Es wird reduziert, wenn wir in Microsoft Word auf den Pfeil neben dem entsprechenden AUTONUMLGL-Feld klicken.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
