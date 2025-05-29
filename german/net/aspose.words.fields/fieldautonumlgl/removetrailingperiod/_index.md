---
title: FieldAutoNumLgl.RemoveTrailingPeriod
linktitle: RemoveTrailingPeriod
articleTitle: RemoveTrailingPeriod
second_title: Aspose.Words für .NET
description: Verwalten Sie die RemoveTrailingPeriod-Eigenschaft von FieldAutoNumLgl, um die Zahlenanzeige anzupassen – entfernen Sie nachfolgende Punkte für eine sauberere, professionelle Formatierung.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

Ruft ab oder legt fest, ob die Zahl ohne abschließenden Punkt angezeigt werden soll.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

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

* class [FieldAutoNumLgl](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
