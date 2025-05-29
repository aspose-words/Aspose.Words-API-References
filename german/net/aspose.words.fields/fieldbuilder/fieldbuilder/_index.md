---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words für .NET
description: Entdecken Sie FieldBuilder, das leistungsstarke Tool zum mühelosen Erstellen und Verwalten von Feldern in Ihren Projekten. Optimieren Sie noch heute Ihren Workflow!
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Initialisiert eine Instanz des[`FieldBuilder`](../) Klasse.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des zu erstellenden Feldes. |

## Beispiele

Zeigt, wie Sie mit einem Feldgenerator ein Feld erstellen und einfügen.

```csharp
Document doc = new Document();

// Eine bequeme Möglichkeit, einem Dokument Textinhalte hinzuzufügen, ist die Verwendung eines Dokumentgenerators.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Felder haben ihren Builder, mit dem wir Stück für Stück einen Feldcode konstruieren können.
// In diesem Fall erstellen wir ein BARCODE-Feld, das eine US-Postleitzahl darstellt,
// und fügen Sie es dann vor einem Run ein.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Siehe auch

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
