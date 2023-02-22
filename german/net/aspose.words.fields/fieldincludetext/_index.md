---
title: Class FieldIncludeText
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fields.FieldIncludeText klas. Implementiert das INCLUDETEXTFeld.
type: docs
weight: 1900
url: /de/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implementiert das INCLUDETEXT-Feld.

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
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname/) { get; set; } | Ruft den Namen des Lesezeichens im einzuschließenden Dokument ab oder legt ihn fest. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ruft den Text ab, der das angezeigte Feldergebnis darstellt. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding/) { get; set; } | Ruft die auf die Daten in der referenzierten Datei angewendete Codierung ab oder legt sie fest. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ruft den Knoten ab, der das Feldende darstellt. |
| [Format](../../aspose.words.fields/field/format/) { get; } | erhält a[`FieldFormat`](../fieldformat/) Objekt, das typisierten Zugriff auf die Feldformatierung bereitstellt. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ruft ab oder legt fest, ob das Feld gesperrt ist (sollte sein Ergebnis nicht neu berechnen). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ruft die LCID des Felds ab oder legt sie fest. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields/) { get; set; } | Ruft ab oder legt fest, ob verhindert werden soll, dass Felder im eingeschlossenen Dokument aktualisiert werden. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype/) { get; set; } | Ruft den MIME-Typ der referenzierten Datei ab oder setzt ihn. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings/) { get; set; } | Ruft die Namespace-Zuordnungen für XPath-Abfragen ab oder legt sie fest. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Liest oder setzt Text, der zwischen dem Feldtrennzeichen und dem Feldende steht. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ruft den Knoten ab, der das Feldtrennzeichen darstellt. Kann null sein. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname/) { get; set; } | Ruft den Speicherort des Dokuments mithilfe eines IRI ab oder legt ihn fest. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ruft den Knoten ab, der den Anfang des Felds darstellt. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter/) { get; set; } | Liest oder setzt den Namen des Textkonverters für das Format der eingebundenen Datei. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ruft den Microsoft Word-Feldtyp ab. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath/) { get; set; } | Ruft XPath für den gewünschten Teil der XML-Datei ab oder legt ihn fest. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation/) { get; set; } | Ruft den Speicherort der XSL-Transformation ab oder legt ihn fest, um XML-Daten zu formatieren. |

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

Fügt den gesamten oder einen Teil des Textes und der Grafiken ein, die in einem anderen Dokument enthalten sind.

### Beispiele

Zeigt, wie ein INCLUDETEXT-Feld erstellt und seine Eigenschaften festgelegt werden.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Im Folgenden finden Sie zwei Möglichkeiten, INCLUDETEXT-Felder zu verwenden, um den Inhalt einer XML-Datei im lokalen Dateisystem anzuzeigen.
    // 1 - Führen Sie eine XSL-Transformation für ein XML-Dokument durch:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Verwenden Sie einen XPath, um bestimmte Elemente aus einem XML-Dokument zu entnehmen:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// Verwenden Sie einen Document Builder, um ein INCLUDETEXT-Feld mit benutzerdefinierten Eigenschaften einzufügen.
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


