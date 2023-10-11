---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Référence de l'API Aspose.Words pour .NET
description: FindReplaceOptions propriété. Obtient ou définit une valeur booléenne indiquant soit dignorer le contenu deStructuredDocumentTag . La valeur par défaut estFAUX .
type: docs
weight: 120
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

Obtient ou définit une valeur booléenne indiquant soit d'ignorer le contenu de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### Remarques

Lorsque cette option est définie sur`vrai` , le contenu de[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) sera traité comme un simple texte.

Sinon,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) sera traité comme Story autonome et le modèle de remplacement sera recherché séparément pour chaque[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), de sorte que si le motif traverse un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , alors le remplacement ne sera pas effectué pour un tel modèle.

### Exemples

Montre comment ignorer le contenu des balises lors du remplacement.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Ce paragraphe contient SDT.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions/)
* Assemblée [Aspose.Words](../../../)


