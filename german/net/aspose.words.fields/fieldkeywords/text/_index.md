---
title: FieldKeywords.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre FieldKeywords ganz einfach! Greifen Sie auf Keyword-Texte zu und passen Sie diese an, um optimale SEO-Leistung und verbesserte Sichtbarkeit zu erzielen.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldkeywords/text/
---
## FieldKeywords.Text property

Ruft den Text der Schlüsselwörter ab oder legt ihn fest.

```csharp
public string Text { get; set; }
```

## Beispiele

Zeigt, wie ein KEYWORDS-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie einige Schlüsselwörter hinzu, die im Datei-Explorer auch als „Tags“ bezeichnet werden.
doc.BuiltInDocumentProperties.Keywords = "Keyword1, Keyword2";

// Das Feld „KEYWORDS“ zeigt den Wert dieser Eigenschaft an.
FieldKeywords field = (FieldKeywords)builder.InsertField(FieldType.FieldKeyword, true);
field.Update();

Assert.AreEqual(" KEYWORDS ", field.GetFieldCode());
Assert.AreEqual("Keyword1, Keyword2", field.Result);

// Festlegen eines Wertes für die Texteigenschaft des Feldes,
// und dann wird durch die Aktualisierung des Felds auch die entsprechende integrierte Eigenschaft mit dem neuen Wert überschrieben.
field.Text = "OverridingKeyword";
field.Update();

Assert.AreEqual(" KEYWORDS  OverridingKeyword", field.GetFieldCode());
Assert.AreEqual("OverridingKeyword", field.Result);
Assert.AreEqual("OverridingKeyword", doc.BuiltInDocumentProperties.Keywords);

doc.Save(ArtifactsDir + "Field.KEYWORDS.docx");
```

### Siehe auch

* class [FieldKeywords](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
