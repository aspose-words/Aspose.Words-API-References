---
title: CopyStylesFromTemplate
second_title: Référence de l'API Aspose.Words pour .NET
description: Copie les styles du modèle spécifié dans un document.
type: docs
weight: 550
url: /fr/net/aspose.words/document/copystylesfromtemplate/
---
## CopyStylesFromTemplate(string) {#copystylesfromtemplate_1}

Copie les styles du modèle spécifié dans un document.

```csharp
public void CopyStylesFromTemplate(string template)
```

### Remarques

Lorsque des styles sont copiés d'un modèle vers un document, les styles portant le même nom dans le document sont redéfinis pour correspondre aux descriptions de style dans le modèle. Les styles uniques du modèle sont copiés vers le document. Les styles uniques du document restent intacts.

### Exemples

Montre comment copier des styles d'un document à un autre.

```csharp
// Crée un document, puis ajoute des styles que nous copierons dans un autre document.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Crée un document dans lequel nous copierons les styles.
Document target = new Document();

// Crée un style portant le même nom qu'un style du document modèle et l'ajoute au document cible.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Il existe deux manières d'appeler la méthode pour copier tous les styles d'un document à l'autre.
// 1 - Passage de l'objet modèle de document :
target.CopyStylesFromTemplate(template);

// La copie des styles ajoute tous les styles du document modèle à la cible
// et écrase les styles existants portant le même nom.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Passage du nom de fichier système local d'un modèle de document :
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## CopyStylesFromTemplate(Document) {#copystylesfromtemplate}

Copie les styles du modèle spécifié dans un document.

```csharp
public void CopyStylesFromTemplate(Document template)
```

### Remarques

Lorsque des styles sont copiés d'un modèle vers un document, les styles portant le même nom dans le document sont redéfinis pour correspondre aux descriptions de style dans le modèle. Les styles uniques du modèle sont copiés vers le document. Les styles uniques du document restent intacts.

### Exemples

Montre comment copier des styles du modèle vers un document via Document.

```csharp
Document template = new Document(MyDir + "Rendering.docx");
Document target = new Document(MyDir + "Document.docx");

target.CopyStylesFromTemplate(template);
```

Montre comment copier des styles d'un document à un autre.

```csharp
// Crée un document, puis ajoute des styles que nous copierons dans un autre document.
Document template = new Document();

Style style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle1");
style.Font.Name = "Times New Roman";
style.Font.Color = Color.Navy;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle2");
style.Font.Name = "Arial";
style.Font.Color = Color.DeepSkyBlue;

style = template.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Courier New";
style.Font.Color = Color.RoyalBlue;

Assert.AreEqual(7, template.Styles.Count);

// Crée un document dans lequel nous copierons les styles.
Document target = new Document();

// Crée un style portant le même nom qu'un style du document modèle et l'ajoute au document cible.
style = target.Styles.Add(StyleType.Paragraph, "TemplateStyle3");
style.Font.Name = "Calibri";
style.Font.Color = Color.Orange;

Assert.AreEqual(5, target.Styles.Count);

// Il existe deux manières d'appeler la méthode pour copier tous les styles d'un document à l'autre.
// 1 - Passage de l'objet modèle de document :
target.CopyStylesFromTemplate(template);

// La copie des styles ajoute tous les styles du document modèle à la cible
// et écrase les styles existants portant le même nom.
Assert.AreEqual(7, target.Styles.Count);

Assert.AreEqual("Courier New", target.Styles["TemplateStyle3"].Font.Name);
Assert.AreEqual(Color.RoyalBlue.ToArgb(), target.Styles["TemplateStyle3"].Font.Color.ToArgb());

// 2 - Passage du nom de fichier système local d'un modèle de document :
target.CopyStylesFromTemplate(MyDir + "Rendering.docx");

Assert.AreEqual(21, target.Styles.Count);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
