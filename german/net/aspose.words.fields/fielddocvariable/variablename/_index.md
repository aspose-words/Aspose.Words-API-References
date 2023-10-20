---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words für .NET
description: FieldDocVariable VariableName eigendom. Ruft den Namen der abzurufenden Dokumentvariablen ab oder legt diesen fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Ruft den Namen der abzurufenden Dokumentvariablen ab oder legt diesen fest.

```csharp
public string VariableName { get; set; }
```

## Beispiele

Zeigt, wie DOCPROPERTY-Felder zum Anzeigen von Dokumenteigenschaften und -variablen verwendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend finden Sie zwei Möglichkeiten zur Verwendung von DOCPROPERTY-Feldern.
// 1 – Eine integrierte Eigenschaft anzeigen:
// Legen Sie einen benutzerdefinierten Wert für die integrierte Eigenschaft „Category“ fest und fügen Sie dann ein DOCPROPERTY-Feld ein, das darauf verweist.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 – Eine benutzerdefinierte Dokumentvariable anzeigen:
// Definieren Sie eine benutzerdefinierte Variable und referenzieren Sie diese Variable dann mit einem DOCPROPERTY-Feld.
Assert.That(doc.Variables, Is.Empty);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Siehe auch

* class [FieldDocVariable](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
