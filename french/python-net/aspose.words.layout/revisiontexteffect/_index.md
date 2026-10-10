---
title: RevisionTextEffect enumeration
linktitle: RevisionTextEffect enumeration
articleTitle: RevisionTextEffect enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.RevisionTextEffect enumeration. Allows to specify decoration effect for revisions of document text."
type: docs
weight: 120
url: /fr/python-net/aspose.words.layout/revisiontexteffect/
---

## RevisionTextEffect enumeration

Allows to specify decoration effect for revisions of document text.


### Members

| Name | Description |
| --- | --- |
| NONE | Revised content has no special effects applied. This corresponds to [RevisionColor.NO_HIGHLIGHT](../revisioncolor/#NO_HIGHLIGHT). |
| COLOR | Revised content is highlighted with color only. |
| BOLD | Revised content is made bold and colored. |
| ITALIC | Revised content is made italic and colored. |
| UNDERLINE | Revised content is underlined and colored. |
| DOUBLE_UNDERLINE | Revised content is double underlined and colored. |
| STRIKE_THROUGH | Revised content is stroked through and colored. |
| DOUBLE_STRIKE_THROUGH | Revised content is double stroked through and colored. |
| HIDDEN | Revised content is hidden. |

### Examples

Shows how to modify the appearance of revisions.

```python
doc = aw.Document(file_name=MY_DIR + 'Revisions.docx')
# Obtenez l'objet RevisionOptions qui contrôle l'apparence des révisions.
revision_options = doc.layout_options.revision_options
# Rendez les révisions d'insertion en vert et en italique.
revision_options.inserted_text_color = aw.layout.RevisionColor.GREEN
revision_options.inserted_text_effect = aw.layout.RevisionTextEffect.ITALIC
# Rendez les révisions de suppression en rouge et en gras.
revision_options.deleted_text_color = aw.layout.RevisionColor.RED
revision_options.deleted_text_effect = aw.layout.RevisionTextEffect.BOLD
# Le même texte apparaîtra deux fois dans une révision de déplacement :
# une fois au point de départ et une fois à la destination d'arrivée.
# Rendez le texte de la révision déplacée depuis en jaune avec un double barré
# et en bleu double-souligné dans la révision déplacée vers.
revision_options.moved_from_text_color = aw.layout.RevisionColor.YELLOW
revision_options.moved_from_text_effect = aw.layout.RevisionTextEffect.DOUBLE_STRIKE_THROUGH
revision_options.moved_to_text_color = aw.layout.RevisionColor.CLASSIC_BLUE
revision_options.moved_to_text_effect = aw.layout.RevisionTextEffect.DOUBLE_UNDERLINE
# Rendez les révisions de format en rouge foncé et en gras.
revision_options.revised_properties_color = aw.layout.RevisionColor.DARK_RED
revision_options.revised_properties_effect = aw.layout.RevisionTextEffect.BOLD
# Placez une barre épaisse bleu foncé sur le côté gauche de la page à côté des lignes affectées par les révisions.
revision_options.revision_bars_color = aw.layout.RevisionColor.DARK_BLUE
revision_options.revision_bars_width = 15
# Affichez les marques de révision et le texte original.
revision_options.show_original_revision = True
revision_options.show_revision_marks = True
# Obtenez les révisions de déplacement, de suppression, de formatage et les commentaires pour qu'ils apparaissent dans des bulles vertes
# sur le côté droit de la page.
revision_options.show_in_balloons = aw.layout.ShowInBalloons.FORMAT
revision_options.comment_color = aw.layout.RevisionColor.BRIGHT_GREEN
# Ces fonctionnalités ne s'appliquent qu'aux formats tels que .pdf ou .jpg.
doc.save(file_name=ARTIFACTS_DIR + 'Revision.RevisionOptions.pdf')
```

### See Also

* module [aspose.words.layout](../)

