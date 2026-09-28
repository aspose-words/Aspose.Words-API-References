---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /fr/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Lorsque nous rédigeons le texte qui ne tient pas sur une page, une ligne peut déborder sur la page suivante.
# La ligne unique qui se retrouve sur la page suivante s’appelle une « Orpheline »,
# et la ligne précédente où l’orpheline s’est détachée s’appelle une « Veuve ».
# Nous pouvons corriger les orphelines et les veuves en réarrangeant le texte via la taille de police, l’espacement ou les marges de page.
# Si nous souhaitons préserver les dimensions de notre document, nous pouvons définir ce drapeau sur "true"
# pour pousser les veuves sur la même page que leurs orphelines respectives.
# Laisser ce drapeau à "false" laissera les paires veuve/orpheline dans le texte.
# Chaque paragraphe possède ce paramètre accessible dans Microsoft Word via Accueil -> Paragraphe -> Paramètres du paragraphe
# (bouton en bas à droite de l’onglet "Paragraph") -> "Contrôle Veuve/Orpheline".
builder.paragraph_format.widow_control = widow_control
# Insérez du texte qui produit une orpheline et une veuve.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

