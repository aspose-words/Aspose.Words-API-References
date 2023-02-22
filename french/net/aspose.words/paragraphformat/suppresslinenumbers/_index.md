---
title: ParagraphFormat.SuppressLineNumbers
second_title: Référence de l'API Aspose.Words pour .NET
description: ParagraphFormat propriété. Spécifie si les lignes du paragraphe actuel doivent être exemptées de la numérotation des lignes qui est appliquée dans la section parent.
type: docs
weight: 370
url: /fr/net/aspose.words/paragraphformat/suppresslinenumbers/
---
## ParagraphFormat.SuppressLineNumbers property

Spécifie si les lignes du paragraphe actuel doivent être exemptées de la numérotation des lignes qui est appliquée dans la section parent.

```csharp
public bool SuppressLineNumbers { get; set; }
```

### Exemples

Montre comment activer la numérotation des lignes pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons utiliser l'objet PageSetup de la section pour afficher les nombres à gauche des lignes de texte de la section.
// C'est le même comportement qu'un objet List,
// mais il couvre toute la section et ne modifie en rien le texte.
// Notre section va recommencer la numérotation à chaque nouvelle page à partir de 1 et afficher le numéro,
// si c'est un multiple de 3, à 50pt à gauche de la ligne.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Le compteur de lignes ignorera tout paragraphe avec le drapeau "SuppressLineNumbers" défini sur "true".
// Ce paragraphe est sur la 15ème ligne, qui est un multiple de 3, et afficherait donc normalement un numéro de ligne.
// Le compteur de lignes de la section ignorera également cette ligne, traitera la ligne suivante comme la 15e,
// et continuer le décompte à partir de ce point.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../paragraphformat/)
* Assemblée [Aspose.Words](../../../)


