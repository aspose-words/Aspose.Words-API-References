---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreHeaderFooter d'ImportFormatOptions, qui contrôle le formatage des en-têtes et pieds de page en mode KeepSourceFormatting. Simplifiez vos importations de documents dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des en-têtes/pieds de page est ignoré siKeepSourceFormatting le mode est utilisé. La valeur par défaut est`vrai` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Exemples

Montre comment spécifier d'ignorer ou non le formatage source du contenu des en-têtes/pieds de page.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Si « IgnoreHeaderFooter » est faux, alors le formatage d'origine du contenu de l'en-tête/pied de page
// à partir de "Types d'en-tête et de pied de page.docx" sera utilisé.
// Si « IgnoreHeaderFooter » est vrai, alors le formatage du contenu de l'en-tête/pied de page
// de "Document.docx" sera utilisé.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
