---
title: RevisionOptions.show_original_revision property
linktitle: show_original_revision property
articleTitle: show_original_revision property
second_title: Aspose.Words for Python
description: "RevisionOptions.show_original_revision property. Allows to specify whether the original text should be shown instead of revised one"
type: docs
weight: 190
url: /fr/python-net/aspose.words.layout/revisionoptions/show_original_revision/
---

## RevisionOptions.show_original_revision property

Allows to specify whether the original text should be shown instead of revised one.
Default value is ``False``.



```python
@property
def show_original_revision(self) -> bool:
    ...

@show_original_revision.setter
def show_original_revision(self, value: bool):
    ...

```

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

* module [aspose.words.layout](../../)
* class [RevisionOptions](../)

