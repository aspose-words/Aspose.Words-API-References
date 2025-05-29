---
title: FieldIncludeText Class
linktitle: FieldIncludeText
articleTitle: FieldIncludeText
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Fields.FieldIncludeText-Klasse für nahtlose Dokumentenintegration. Verbessern Sie Ihren Workflow mit der effizienten Implementierung von INCLUDETEXT-Feldern.
type: docs
weight: 2460
url: /de/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implementiert das Feld INCLUDETEXT.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class FieldIncludeText : Field
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FieldIncludeText](fieldincludetext/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Ruft den Namen des einzuschließenden Lesezeichens im Dokument ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Ruft die auf die Daten in der referenzierten Datei angewendete Kodierung ab oder legt sie fest. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Erhält eine[`FieldFormat`](../fieldformat/)Objekt, das typisierten Zugriff auf die Formatierung des Felds bietet. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (das Ergebnis sollte nicht neu berechnet werden). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Ruft ab oder legt fest, ob die Aktualisierung von Feldern im eingeschlossenen Dokument verhindert werden soll. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Ruft den MIME-Typ der referenzierten Datei ab oder legt ihn fest. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Ruft die Namespace-Zuordnungen für XPath-Abfragen ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ruft Text ab oder legt ihn fest, der zwischen Feldtrennzeichen und Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann sein`null` . |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Ruft den Speicherort des Dokuments mithilfe eines IRI ab oder legt ihn fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Ruft den Namen des Textkonverters für das Format der eingebundenen Datei ab oder legt ihn fest. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Ruft XPath für den gewünschten Teil der XML-Datei ab oder legt ihn fest. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Ruft den Speicherort der XSL-Transformation zum Formatieren von XML-Daten ab oder legt ihn fest. |

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

Fügt den gesamten oder einen Teil des Textes und der Grafiken ein, die in einem anderen Dokument enthalten sind.

## Beispiele

Zeigt, wie Sie ein INCLUDETEXT-Feld erstellen und seine Eigenschaften festlegen.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Unten sind zwei Möglichkeiten zur Verwendung von INCLUDETEXT-Feldern aufgeführt, um den Inhalt einer XML-Datei im lokalen Dateisystem anzuzeigen.
    // 1 – Führen Sie eine XSL-Transformation an einem XML-Dokument durch:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 – Verwenden Sie einen XPath, um bestimmte Elemente aus einem XML-Dokument zu übernehmen:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Verwenden Sie einen Dokumentgenerator, um ein INCLUDETEXT-Feld mit benutzerdefinierten Eigenschaften einzufügen.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Siehe auch

* class [Field](../field/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
