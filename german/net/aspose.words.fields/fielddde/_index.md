---
title: Class FieldDde
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldDde klas. Implementiert das DDEFeld.
type: docs
weight: 1630
url: /de/net/aspose.words.fields/fielddde/
---
## FieldDde class

Implementiert das DDE-Feld.

```csharp
public class FieldDde : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldDde](fielddde/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AutoUpdate](../../aspose.words.fields/fielddde/autoupdate/) { get; set; } | Ruft ab oder legt fest, ob dieses Feld automatisch aktualisiert werden soll. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [InsertAsBitmap](../../aspose.words.fields/fielddde/insertasbitmap/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt als Bitmap eingefügt werden soll. |
| [InsertAsHtml](../../aspose.words.fields/fielddde/insertashtml/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt als Text im HTML-Format eingefügt werden soll. |
| [InsertAsPicture](../../aspose.words.fields/fielddde/insertaspicture/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt als Bild eingefügt werden soll. |
| [InsertAsRtf](../../aspose.words.fields/fielddde/insertasrtf/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt im Rich-Text-Format (RTF) eingefügt werden soll. |
| [InsertAsText](../../aspose.words.fields/fielddde/insertastext/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt im Nur-Text-Format eingefügt werden soll. |
| [InsertAsUnicode](../../aspose.words.fields/fielddde/insertasunicode/) { get; set; } | Ruft ab oder legt fest, ob das verknüpfte Objekt als Unicode-Text eingefügt werden soll. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLinked](../../aspose.words.fields/fielddde/islinked/) { get; set; } | Ruft ab oder legt fest, ob die Dateigröße reduziert werden soll, indem keine Grafikdaten mit dem Dokument gespeichert werden. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [ProgId](../../aspose.words.fields/fielddde/progid/) { get; set; } | Ruft den Anwendungstyp der Linkinformationen ab oder legt ihn fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SourceFullName](../../aspose.words.fields/fielddde/sourcefullname/) { get; set; } | Ruft den Namen und Speicherort der Quelldatei ab oder legt ihn fest. |
| [SourceItem](../../aspose.words.fields/fielddde/sourceitem/) { get; set; } | Ruft den Teil der Quelldatei ab, der verknüpft wird, oder legt ihn fest. |
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

Bei Informationen, die aus einer anderen Anwendung kopiert wurden, verknüpft dieses Feld diese Informationen mithilfe von DDE mit der ursprünglichen Quelldatei.

### Beispiele

Zeigt, wie Sie verschiedene Feldtypen verwenden, um auf andere Dokumente im lokalen Dateisystem zu verlinken und deren Inhalt anzuzeigen.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Unten sind drei Arten von Feldern, die wir verwenden können, um Inhalte aus einem verknüpften Dokument in Form von Text anzuzeigen.
    // 1 - Ein LINK-Feld:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", MyDir + "Document.docx", null, true);

    // 2 - Ein DDE-Feld:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Ein DDEAUTO-Feld:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.docx");
}

{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Unten sind drei Arten von Feldern, die wir verwenden können, um Inhalte aus einem verknüpften Dokument in Form eines Bildes anzuzeigen.
    // 1 - Ein LINK-Feld:
    builder.Writeln("FieldLink:\n");
    InsertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "MySpreadsheet.xlsx",
        "Sheet1!R2C2", true);

    // 2 - Ein DDE-Feld:
    builder.Writeln("FieldDde:\n");
    InsertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true, true);

    // 3 - Ein DDEAUTO-Feld:
    builder.Writeln("FieldDdeAuto:\n");
    InsertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", MyDir + "Spreadsheet.xlsx",
        "Sheet1!R1C1", true);

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
}

/// <summary>
/// Verwenden Sie einen Document Builder, um ein LINK-Feld einzufügen und seine Eigenschaften gemäß Parametern festzulegen.
/// </summary>
private static void InsertFieldLink(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool shouldAutoUpdate)
{
    FieldLink field = (FieldLink)builder.InsertField(FieldType.FieldLink, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;

    builder.Writeln("\n");
}

/// <summary>
/// Verwenden Sie einen Document Builder, um ein DDE-Feld einzufügen, und legen Sie seine Eigenschaften gemäß Parametern fest.
/// </summary>
private static void InsertFieldDde(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs, string progId,
    string sourceFullName, string sourceItem, bool isLinked, bool shouldAutoUpdate)
{
    FieldDde field = (FieldDde)builder.InsertField(FieldType.FieldDDE, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.AutoUpdate = shouldAutoUpdate;
    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;

    builder.Writeln("\n");
}

/// <summary>
/// Verwenden Sie einen Document Builder, um ein DDEAUTO-Feld einzufügen und seine Eigenschaften gemäß Parametern festzulegen.
/// </summary>
private static void InsertFieldDdeAuto(DocumentBuilder builder, InsertLinkedObjectAs insertLinkedObjectAs,
    string progId, string sourceFullName, string sourceItem, bool isLinked)
{
    FieldDdeAuto field = (FieldDdeAuto)builder.InsertField(FieldType.FieldDDEAuto, true);

    switch (insertLinkedObjectAs)
    {
        case InsertLinkedObjectAs.Text:
            field.InsertAsText = true;
            break;
        case InsertLinkedObjectAs.Unicode:
            field.InsertAsUnicode = true;
            break;
        case InsertLinkedObjectAs.Html:
            field.InsertAsHtml = true;
            break;
        case InsertLinkedObjectAs.Rtf:
            field.InsertAsRtf = true;
            break;
        case InsertLinkedObjectAs.Picture:
            field.InsertAsPicture = true;
            break;
        case InsertLinkedObjectAs.Bitmap:
            field.InsertAsBitmap = true;
            break;
    }

    field.ProgId = progId;
    field.SourceFullName = sourceFullName;
    field.SourceItem = sourceItem;
    field.IsLinked = isLinked;
}

public enum InsertLinkedObjectAs
{
    // LinkedObjectAsText
    Text,
    Unicode,
    Html,
    Rtf,
    // LinkedObjectAsImage
    Picture,
    Bitmap
}
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)


