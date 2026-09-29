---
title: Revision.parent_node property
linktitle: parent_node property
articleTitle: parent_node property
second_title: Aspose.Words for Python
description: "Revision.parent_node property. Gets the immediate parent node (owner) of this revision"
type: docs
weight: 40
url: /sv/python-net/aspose.words/revision/parent_node/
---

## Revision.parent_node property

Gets the immediate parent node (owner) of this revision.
This property will work for any revision type other than [RevisionType.STYLE_DEFINITION_CHANGE](../../revisiontype/#STYLE_DEFINITION_CHANGE).



```python
@property
def parent_node(self) -> aspose.words.Node:
    ...

```

### Remarks

If this revision relates to change of Style formatting, use [Revision.parent_style](../parent_style/) instead.



### Examples

Shows how to determine the revision type of an inline node.

```python
doc = aw.Document(file_name=MY_DIR + 'Revision runs.docx')
# När vi redigerar dokumentet medan "Track Changes"-alternativet, som finns via Review -> Tracking,
# är påslaget i Microsoft Word, räknas de ändringar vi gör som revisioner.
# När vi redigerar ett dokument med Aspose.Words kan vi börja spåra revisioner genom att
# anropa dokumentets "StartTrackRevisions"-metod och sluta spåra genom att använda "StopTrackRevisions"-metoden.
# Vi kan antingen acceptera revisioner för att införliva dem i dokumentet
# eller avvisa dem för att effektivt ändra den föreslagna förändringen.
self.assertEqual(6, doc.revisions.count)
# Föräldranoden för en revision är den run som revisionen gäller. En Run är en Inline-nod.
run = doc.revisions[0].parent_node.as_run()
first_paragraph = run.parent_paragraph
runs = first_paragraph.runs
self.assertEqual(6, len(list(runs)))
# Nedan följer fem typer av revisioner som kan flagga en Inline-nod.
# 1 -  En "insert"-revision:
# Denna revision uppstår när vi infogar text medan vi spårar ändringar.
self.assertTrue(runs[2].is_insert_revision)
# 2 -  En "format"-revision:
# Denna revision uppstår när vi ändrar formateringen av text medan vi spårar ändringar.
self.assertTrue(runs[2].is_format_revision)
# 3 -  En "move from"-revision:
# När vi markerar text i Microsoft Word och sedan drar den till en annan plats i dokumentet
# medan vi spårar ändringar, visas två revisioner.
# "move from"-revisionen är en kopia av texten som ursprungligen fanns innan vi flyttade den.
self.assertTrue(runs[4].is_move_from_revision)
# 4 -  En "move to"-revision:
# "move to"-revisionen är den text som vi flyttade till sin nya position i dokumentet.
# "Move from"- och "move to"-revisioner visas i par för varje flyttrevision vi utför.
# Att acceptera en flyttrevision tar bort "move from"-revisionen och dess text,
# och behåller texten från "move to"-revisionen.
# Att avvisa en flyttrevision behåller däremot "move from"-revisionen och tar bort "move to"-revisionen.
self.assertTrue(runs[1].is_move_to_revision)
# 5 -  En "delete"-revision:
# Denna revision uppstår när vi tar bort text medan vi spårar ändringar. När vi tar bort text på detta sätt,
# kommer den att finnas kvar i dokumentet som en revision tills vi antingen accepterar revisionen,
# vilket kommer att radera texten permanent, eller avvisa revisionen, vilket kommer att behålla den text vi raderade där den var.
self.assertTrue(runs[5].is_delete_revision)
```

### See Also

* module [aspose.words](../../)
* class [Revision](../)

