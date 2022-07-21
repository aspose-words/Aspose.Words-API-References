---
title: Add
second_title: Aspose.Words für .NET-API-Referenz
description: Fügt der Sammlung ein Element hinzu.
type: docs
weight: 40
url: /de/net/aspose.words.markup/customxmlpartcollection/add/
---
## Add(CustomXmlPart) {#add_1}

Fügt der Sammlung ein Element hinzu.

```csharp
public void Add(CustomXmlPart part)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| part | CustomXmlPart | Der benutzerdefinierte XML-Teil, der hinzugefügt werden soll. |

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

* class [CustomXmlPart](../../customxmlpart)
* class [CustomXmlPartCollection](../../customxmlpartcollection)
* namensraum [Aspose.Words.Markup](../../customxmlpartcollection)
* Montage [Aspose.Words](../../../)

---

## Add(string, string) {#add}

Erstellt einen neuen XML-Teil mit dem angegebenen XML und fügt ihn der Sammlung hinzu.

```csharp
public CustomXmlPart Add(string id, string xml)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | String | Bezeichner eines neuen benutzerdefinierten XML-Teils. |
| xml | String | XML-Daten des Teils. |

### Rückgabewert

Benutzerdefiniertes XML-Teil erstellt.

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

* class [CustomXmlPart](../../customxmlpart)
* class [CustomXmlPartCollection](../../customxmlpartcollection)
* namensraum [Aspose.Words.Markup](../../customxmlpartcollection)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
