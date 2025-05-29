---
title: EditableRange.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words pour .NET
description: Découvrez la propriété EditableRange Id, accédez et gérez facilement vos identifiants de plage modifiables pour un contrôle et une efficacité améliorés des documents.
type: docs
weight: 40
url: /fr/net/aspose.words/editablerange/id/
---
## EditableRange.Id property

Obtient l'identifiant de plage modifiable.

```csharp
public int Id { get; }
```

## Remarques

La région doit être délimitée à l'aide de la[`EditableRangeStart`](../editablerangestart/) et[`EditableRangeEnd`](../editablerangeend/)

Les identifiants de plage modifiables sont censés être uniques dans un document et Aspose.Words conserve automatiquement les identifiants de plage modifiables lors du chargement, de l'enregistrement et de la combinaison de documents.

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

* class [EditableRange](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
