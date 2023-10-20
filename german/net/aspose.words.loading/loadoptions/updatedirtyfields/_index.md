---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words für .NET
description: LoadOptions UpdateDirtyFields eigendom. Gibt an ob die Felder mit aktualisiert werden sollenschmutzig attribute in C#.
type: docs
weight: 160
url: /de/net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Gibt an, ob die Felder mit aktualisiert werden sollen`schmutzig` attribute.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Beispiele

Zeigt, wie eine spezielle Eigenschaft zum Aktualisieren des Feldergebnisses verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie den integrierten Eigenschaftswert „Autor“ des Dokuments an und zeigen Sie ihn dann mit einem Feld an.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.False(field.IsDirty);
Assert.AreEqual("John Doe", field.Result);

// Die Eigenschaft aktualisieren. Das Feld zeigt weiterhin den alten Wert an.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.AreEqual("John Doe", field.Result);

// Da der Feldwert veraltet ist, können wir ihn als „schmutzig“ markieren.
// Dieser Wert bleibt veraltet, bis wir das Feld manuell mit der Field.Update()-Methode aktualisieren.
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // Wenn wir speichern, ohne eine Update-Methode aufzurufen,
    // Das Feld zeigt weiterhin den veralteten Wert im Ausgabedokument an.
    doc.Save(docStream, SaveFormat.Docx);

    // Das LoadOptions-Objekt verfügt über eine Option zum Aktualisieren aller Felder
    // Beim Laden des Dokuments als „dirty“ markiert.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.AreEqual("John & Jane Doe", doc.BuiltInDocumentProperties.Author);

    field = (FieldAuthor)doc.Range.Fields[0];

    // Beim Aktualisieren solcher Dirty-Felder wird ihr „IsDirty“-Flag automatisch auf „false“ gesetzt.
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
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
