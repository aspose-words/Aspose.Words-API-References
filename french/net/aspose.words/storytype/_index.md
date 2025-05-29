---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.StoryType et gérez facilement et efficacement les histoires textuelles de vos documents Word. Améliorez votre expérience de traitement de documents dès aujourd'hui !
type: docs
weight: 6970
url: /fr/net/aspose.words/storytype/
---
## StoryType enumeration

Le texte d'un document Word est stocké dans des histoires.`StoryType` identifie une histoire.

```csharp
public enum StoryType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Valeur par défaut. Ce récit n'existe pas dans le document. |
| MainText | `1` | Contient le texte principal du document, représenté par[`Body`](../body/) . |
| Footnotes | `2` | Contient un texte de note de bas de page, représenté par[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Contient du texte de notes de fin, représenté par[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Contient des commentaires de document (annotations), représentés par[`Comment`](../comment/) . |
| Textbox | `5` | Contient une forme ou un texte de zone de texte, représenté par[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Contient le texte de l'en-tête des pages paires, représenté par[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Contient le texte de l'en-tête principal. Lorsque l'en-tête diffère pour les pages paires et impaires, contient le texte de l'en-tête des pages impaires. Représenté par[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Contient le texte du pied de page des pages paires, représenté par[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Contient le texte du pied de page principal. Lorsque le pied de page est différent pour les pages paires et impaires, contient le texte du pied de page des pages impaires. Représenté par[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Contient le texte de l'en-tête de la première page, représenté par[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Contient le texte du pied de page de la première page, représenté par[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Contient le texte du séparateur de note de bas de page. |
| FootnoteContinuationSeparator | `13` | Contient le texte du séparateur de continuation de note de bas de page. |
| FootnoteContinuationNotice | `14` | Contient le texte du séparateur d'avis de continuation de note de bas de page. |
| EndnoteSeparator | `15` | Contient le texte du séparateur de note de fin. |
| EndnoteContinuationSeparator | `16` | Contient le texte du séparateur de continuation de note de fin. |
| EndnoteContinuationNotice | `17` | Contient le texte du séparateur de l'avis de continuation de note de fin. |

## Exemples

Montre comment supprimer toutes les formes d'un nœud.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne.
// qui a un paragraphe parent, qui est un nœud enfant du corps de la première section.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce corps.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
