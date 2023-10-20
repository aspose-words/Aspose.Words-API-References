---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words pour .NET
description: DocumentBuilder InsertFootnote méthode. Insère une note de bas de page ou de fin dans le document en C#.
type: docs
weight: 330
url: /fr/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Insère une note de bas de page ou de fin dans le document.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| footnoteType | FootnoteType | Spécifie s’il faut insérer une note de bas de page ou une note de fin. |
| footnoteText | String | Spécifie le texte de la note de bas de page. |

### Return_Value

Renvoie un objet note de bas de page qui vient d'être créé.

## Exemples

Montre comment référencer du texte avec une note de bas de page et une note de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère du texte et marque-le avec une note de bas de page avec la propriété IsAuto définie sur "true" par défaut,
// donc le marqueur vu dans le corps du texte sera automatiquement numéroté à "1",
// et la note de bas de page apparaîtra en bas de la page.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insère plus de texte et marque-le avec une note de fin avec une marque de référence personnalisée,
// qui sera utilisé à la place du chiffre "2" et définira "IsAuto" sur false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Les notes de bas de page apparaissent toujours en bas de leur texte référencé,
// donc ce saut de page n'affectera pas la note de bas de page.
// Par contre, les notes de fin sont toujours à la fin du document
// pour que ce saut de page pousse la note de fin vers la page suivante.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Voir également

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Insère une note de bas de page ou de fin dans le document.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| footnoteType | FootnoteType | Spécifie s’il faut insérer une note de bas de page ou une note de fin. |
| footnoteText | String | Spécifie le texte de la note de bas de page. |
| referenceMark | String | Spécifie la marque de référence personnalisée de la note de bas de page. |

### Return_Value

Renvoie un objet note de bas de page qui vient d'être créé.

## Exemples

Montre comment référencer du texte avec une note de bas de page et une note de fin.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère du texte et marque-le avec une note de bas de page avec la propriété IsAuto définie sur "true" par défaut,
// donc le marqueur vu dans le corps du texte sera automatiquement numéroté à "1",
// et la note de bas de page apparaîtra en bas de la page.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insère plus de texte et marque-le avec une note de fin avec une marque de référence personnalisée,
// qui sera utilisé à la place du chiffre "2" et définira "IsAuto" sur false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Les notes de bas de page apparaissent toujours en bas de leur texte référencé,
// donc ce saut de page n'affectera pas la note de bas de page.
// Par contre, les notes de fin sont toujours à la fin du document
// pour que ce saut de page pousse la note de fin vers la page suivante.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Voir également

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
