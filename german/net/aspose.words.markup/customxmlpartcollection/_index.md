---
title: CustomXmlPartCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert eine Sammlung benutzerdefinierter XML-Teile. Die Artikel sindCustomXmlPart./customxmlpart Objekte.
type: docs
weight: 3690
url: /de/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Repräsentiert eine Sammlung benutzerdefinierter XML-Teile. Die Artikel sind[`CustomXmlPart`](../customxmlpart) Objekte.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item) { get; set; } | Ruft ein Element am angegebenen Index ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add#add_1)(CustomXmlPart) | Fügt der Sammlung ein Element hinzu. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add#add)(string, string) | Erstellt einen neuen XML-Teil mit dem angegebenen XML und fügt ihn der Sammlung hinzu. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear)() | Entfernt alle Elemente aus der Sammlung. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone)() | Erstellt eine tiefe Kopie dieser Sammlung und ihrer Elemente. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid)(string) | Sucht und gibt einen benutzerdefinierten XML-Teil anhand seines Bezeichners zurück. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator)() | Gibt ein Aufzählungsobjekt zurück, das verwendet werden kann, um alle Elemente in der Sammlung zu durchlaufen. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat)(int) | Entfernt ein Element am angegebenen Index. |

### Bemerkungen

Normalerweise müssen Sie keine Instanzen dieser Klasse erstellen. Sie können über die in einem Dokument gespeicherten benutzerdefinierten XML-Daten zugreifen[`CustomXmlParts`](../../aspose.words/document/customxmlparts) Eigentum.

### Beispiele

Zeigt, wie ein strukturiertes Dokument-Tag mit benutzerdefinierten XML-Daten erstellt wird.

```csharp
Document doc = new Document();

// Erstellen Sie einen XML-Teil, der Daten enthält, und fügen Sie ihn der Sammlung des Dokuments hinzu.
// Wenn wir die Registerkarte "Entwickler" in Microsoft Word aktivieren,
// Wir können Elemente aus dieser Sammlung zusammen mit einigen Standardelementen im "XML Mapping Pane" finden.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Im Folgenden finden Sie zwei Möglichkeiten, auf XML-Teile zu verweisen.
// 1 - Durch einen Index in der benutzerdefinierten XML-Teilsammlung:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Nach GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Eine XML-Schemazuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klonen Sie einen Teil und fügen Sie ihn dann in die Sammlung ein.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Iteriere durch die Sammlung und drucke den Inhalt jedes Teils.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Verwenden Sie die Methode "RemoveAt", um den geklonten Teil nach Index zu entfernen.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klonen Sie die XML-Teilesammlung und verwenden Sie dann die "Clear"-Methode, um alle ihre Elemente auf einmal zu entfernen.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres Teils anzeigt, und fügen Sie es in den Dokumentkörper ein.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Siehe auch

* class [CustomXmlPart](../customxmlpart)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
