---
title: EditableRangeStart.EditableRange
linktitle: EditableRange
articleTitle: EditableRange
second_title: Aspose.Words pour .NET
description: Découvrez la propriété EditableRangeStart, la clé pour gérer facilement les plages modifiables. Accédez et contrôlez votre contenu en toute simplicité !
type: docs
weight: 10
url: /fr/net/aspose.words/editablerangestart/editablerange/
---
## EditableRangeStart.EditableRange property

Obtient l'objet de façade qui encapsule cette plage modifiable de début et de fin.

```csharp
public EditableRange EditableRange { get; }
```

## Exemples

Montre comment travailler avec une plage modifiable.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only," +
                " we cannot edit this paragraph without the password.");

// Les plages modifiables nous permettent de laisser des parties de documents protégés ouvertes pour modification.
EditableRangeStart editableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph is inside an editable range, and can be edited.");
EditableRangeEnd editableRangeEnd = builder.EndEditableRange();

// Une plage modifiable bien formée possède un nœud de départ et un nœud de fin.
// Ces nœuds ont des identifiants correspondants et englobent des nœuds modifiables.
EditableRange editableRange = editableRangeStart.EditableRange;

Assert.AreEqual(editableRangeStart.Id, editableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.Id);

// Différentes parties de la plage modifiable sont liées les unes aux autres.
Assert.AreEqual(editableRangeStart.Id, editableRange.EditableRangeStart.Id);
Assert.AreEqual(editableRangeStart.Id, editableRangeEnd.EditableRangeStart.Id);
Assert.AreEqual(editableRange.Id, editableRangeStart.EditableRange.Id);
Assert.AreEqual(editableRangeEnd.Id, editableRange.EditableRangeEnd.Id);

// Nous pouvons accéder aux types de nœuds de chaque partie de cette manière. La plage modifiable elle-même n'est pas un nœud.
// mais une entité qui se compose d'un début, d'une fin et de leur contenu inclus.
Assert.AreEqual(NodeType.EditableRangeStart, editableRangeStart.NodeType);
Assert.AreEqual(NodeType.EditableRangeEnd, editableRangeEnd.NodeType);

builder.Writeln("This paragraph is outside the editable range, and cannot be edited.");

doc.Save(ArtifactsDir + "EditableRange.CreateAndRemove.docx");

// Supprimer une plage modifiable. Tous les nœuds contenus dans la plage resteront intacts.
editableRange.Remove();
```

### Voir également

* class [EditableRange](../../editablerange/)
* class [EditableRangeStart](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
