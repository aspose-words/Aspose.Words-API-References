---
title: EditableRangeEnd.EditableRangeStart
linktitle: EditableRangeStart
articleTitle: EditableRangeStart
second_title: Aspose.Words pour .NET
description: EditableRangeEnd EditableRangeStart propriété. CorrespondantEditableRangeStart  reçu par ID en C#.
type: docs
weight: 10
url: /fr/net/aspose.words/editablerangeend/editablerangestart/
---
## EditableRangeEnd.EditableRangeStart property

Correspondant[`EditableRangeStart`](../../editablerangestart/) , reçu par ID.

```csharp
public EditableRangeStart EditableRangeStart { get; }
```

## Exemples

Montre comment travailler avec une plage modifiable.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Les plages modifiables nous permettent de laisser des parties de documents protégés ouvertes pour l'édition.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Une plage modifiable bien formée a un nœud de début et un nœud de fin.
// Ces nœuds ont des ID correspondants et englobent des nœuds modifiables.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Différentes parties de la plage modifiable sont liées les unes aux autres.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Nous pouvons accéder aux types de nœuds de chaque partie comme ceci. La plage modifiable elle-même n'est pas un nœud,
// mais une entité composée d'un début, d'une fin et de leur contenu inclus.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Supprime une plage modifiable. Tous les nœuds qui se trouvaient à l'intérieur de la plage resteront intacts.
editableRange.Remove();
```

### Voir également

* class [EditableRangeStart](../../editablerangestart/)
* class [EditableRangeEnd](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
