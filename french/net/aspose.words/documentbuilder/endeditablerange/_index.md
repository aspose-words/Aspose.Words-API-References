---
title: DocumentBuilder.EndEditableRange
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Marque la position actuelle dans le document comme une fin de plage modifiable.
type: docs
weight: 210
url: /fr/net/aspose.words/documentbuilder/endeditablerange/
---
## EndEditableRange() {#endeditablerange}

Marque la position actuelle dans le document comme une fin de plage modifiable.

```csharp
public EditableRangeEnd EndEditableRange()
```

### Return_Value

Le nœud de fin de plage modifiable qui vient d'être créé.

### Remarques

La plage modifiable dans un document peut chevaucher et s'étendre sur n'importe quelle plage. Pour créer une plage modifiable valide, vous devez appeler les deux[`StartEditableRange`](../starteditablerange/) et`EndEditableRange` ou`EndEditableRange`méthodes.

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

### Exemples

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

* class [EditableRangeEnd](../../editablerangeend/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## EndEditableRange(EditableRangeStart) {#endeditablerange_1}

Marque la position actuelle dans le document comme une fin de plage modifiable.

```csharp
public EditableRangeEnd EndEditableRange(EditableRangeStart start)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| start | EditableRangeStart | Cette plage modifiable commence. |

### Return_Value

Le nœud de fin de plage modifiable qui vient d'être créé.

### Remarques

Utilisez cette surcharge lors de la création de plages modifiables imbriquées.

La plage modifiable dans un document peut chevaucher et s'étendre sur n'importe quelle plage. Pour créer une plage modifiable valide, vous devez appeler les deux[`StartEditableRange`](../starteditablerange/) et`EndEditableRange` ou`EndEditableRange`méthodes.

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

### Exemples

Montre comment créer des plages modifiables imbriquées.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "MyPassword");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world! Since we have set the document's protection level to read-only, " +
                "we cannot edit this paragraph without the password.");

// Crée deux plages modifiables imbriquées.
EditableRangeStart outerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside the outer editable range and can be edited.");

EditableRangeStart innerEditableRangeStart = builder.StartEditableRange();
builder.Writeln("This paragraph inside both the outer and inner editable ranges and can be edited.");

// Actuellement, le curseur d'insertion de nœud du générateur de document se trouve dans plusieurs plages modifiables en cours.
// Lorsque nous voulons terminer une plage modifiable dans cette situation,
// nous devons spécifier laquelle des plages nous souhaitons terminer en passant son nœud EditableRangeStart.
builder.EndEditableRange(innerEditableRangeStart);

builder.Writeln("This paragraph inside the outer editable range and can be edited.");

builder.EndEditableRange(outerEditableRangeStart);

builder.Writeln("This paragraph is outside any editable ranges, and cannot be edited.");

// Si une zone de texte a deux plages modifiables qui se chevauchent avec des groupes spécifiés,
// le groupe combiné d'utilisateurs exclus par les deux groupes ne peut pas le modifier.
outerEditableRangeStart.EditableRange.EditorGroup = EditorType.Everyone;
innerEditableRangeStart.EditableRange.EditorGroup = EditorType.Contributors;

doc.Save(ArtifactsDir + "EditableRange.Nested.docx");
```

### Voir également

* class [EditableRangeEnd](../../editablerangeend/)
* class [EditableRangeStart](../../editablerangestart/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


