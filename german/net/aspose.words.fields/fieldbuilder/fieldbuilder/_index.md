---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words für .NET
description: FieldBuilder constructeur. Initialisiert eine Instanz vonFieldBuilder Klasse in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Initialisiert eine Instanz von[`FieldBuilder`](../) Klasse.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | FieldType | Der Typ des zu erstellenden Feldes. |

## Beispiele

Zeigt, wie man ein Feld mit einem Feld-Builder erstellt und einfügt.

```csharp
Document doc = new Document();

// Eine bequeme Möglichkeit, Textinhalte zu einem Dokument hinzuzufügen, ist die Verwendung eines Document Builders.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Felder haben ihren Builder, mit dem wir Stück für Stück einen Feldcode erstellen können.
// In diesem Fall erstellen wir ein BARCODE-Feld, das eine US-Postleitzahl darstellt.
// und dann vor einem Run einfügen.
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
