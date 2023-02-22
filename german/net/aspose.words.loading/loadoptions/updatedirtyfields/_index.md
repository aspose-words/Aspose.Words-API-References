---
title: LoadOptions.UpdateDirtyFields
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Gibt an ob die Felder mit aktualisiert werden sollenschmutzig Attribut.
type: docs
weight: 160
url: /de/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` Attribut.

```csharp
public bool UpdateDirtyFields { get; set; }
```

### Beispiele

Zeigt, wie eine spezielle Eigenschaft zum Aktualisieren von Feldergebnissen verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie den integrierten "Autor"-Eigenschaftswert des Dokuments an und zeigen Sie ihn dann mit einem Feld an.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Eigenschaft aktualisieren. Das Feld zeigt noch den alten Wert an.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Da der Wert des Feldes veraltet ist, können wir ihn als "dirty" markieren.
// Dieser Wert bleibt veraltet, bis wir das Feld manuell mit der Methode Field.Update() aktualisieren.
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Wenn wir speichern, ohne eine Update-Methode aufzurufen,
    // Das Feld zeigt weiterhin den veralteten Wert im Ausgabedokument an.
    doc.Save(docStream, SaveFormat.Docx);

    // Das LoadOptions-Objekt hat eine Option zum Aktualisieren aller Felder
    // beim Laden des Dokuments als "dirty" markiert.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Das Aktualisieren von Dirty-Feldern wie diesem setzt ihr "IsDirty"-Flag automatisch auf "false".
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

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


