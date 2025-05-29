---
title: FieldMergingArgsBase.FieldValue
linktitle: FieldValue
articleTitle: FieldValue
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldValue-Eigenschaft von FieldMergingArgsBase. Greifen Sie einfach auf Feldwerte aus Ihrer Datenquelle zu und ändern Sie diese für ein verbessertes Datenmanagement.
type: docs
weight: 50
url: /de/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

Ruft den Wert des Felds aus der Datenquelle ab oder legt ihn fest.

```csharp
public object FieldValue { get; set; }
```

## Bemerkungen

Diese Eigenschaft enthält einen Wert, der vom Serienbriefmodul aus Ihrer Datenquelle für dieses Feld ausgewählt wurde. Sie können den Wert auch durch Festlegen der Eigenschaft ersetzen.

## Beispiele

Zeigt, wie Werte bearbeitet werden, die MERGEFIELDs beim Seriendruck erhalten.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Fügen Sie einige MERGEFIELDs mit Formatschaltern ein, die die Werte bearbeiten, die sie während eines Seriendrucks erhalten.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// Bearbeitet die Werte, die MERGEFIELDs während eines Serienbriefs erhalten.
/// Der Name eines MERGEFIELD muss ein Präfix haben, damit dieser Rückruf auf seinen Wert angewendet wird.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// Wird aufgerufen, wenn ein Serienbrief Daten in ein MERGEFIELD zusammenführt.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // Nichts tun.
    }
}
```

### Siehe auch

* class [FieldMergingArgsBase](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
