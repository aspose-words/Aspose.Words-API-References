---
title: Field.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words für .NET
description: Verwalten Sie die IsDirty-Eigenschaft, um sicherzustellen, dass Ihre Felddaten genau und aktuell bleiben, und verbessern Sie so die Dokumentintegrität und Leistung.
type: docs
weight: 40
url: /de/net/aspose.words.fields/field/isdirty/
---
## Field.IsDirty property

Ruft ab oder legt fest, ob das aktuelle Ergebnis des Felds aufgrund anderer am Dokument vorgenommener Änderungen nicht mehr korrekt (veraltet) ist.

```csharp
public bool IsDirty { get; set; }
```

## Beispiele

Zeigt, wie spezielle Eigenschaften zum Aktualisieren von Feldergebnissen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie den integrierten Eigenschaftswert „Autor“ des Dokuments an und zeigen Sie ihn dann mit einem Feld an.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Aktualisieren Sie die Eigenschaft. Das Feld zeigt weiterhin den alten Wert an.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Da der Wert des Felds veraltet ist, können wir es als „schmutzig“ markieren.
// Dieser Wert bleibt veraltet, bis wir das Feld manuell mit der Methode Field.Update() aktualisieren.
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Wenn wir speichern, ohne eine Update-Methode aufzurufen,
    // Das Feld zeigt im Ausgabedokument weiterhin den veralteten Wert an.
    doc.Save(docStream, SaveFormat.Docx);

    // Das LoadOptions-Objekt verfügt über eine Option zum Aktualisieren aller Felder
    // beim Laden des Dokuments als „dirty“ markiert.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Durch das Aktualisieren von schmutzigen Feldern wie diesem wird deren Flag „IsDirty“ automatisch auf „false“ gesetzt.
    if (updateDirtyFields)
    {
        Assert.AreEqual("John & Jane Doe", field.Result);
        Assert.False(field.IsDirty);
    }
    else
    {
        Assert.AreEqual("John Doe", field.Result);
        Assert.True(field.IsDirty);
    }
}
```

### Siehe auch

* class [Field](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
