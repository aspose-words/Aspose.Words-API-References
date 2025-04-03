---
title: List.isRestartAtEachSection property
linktitle: isRestartAtEachSection property
articleTitle: isRestartAtEachSection property
second_title: Aspose.Words for NodeJs
description: "List.isRestartAtEachSection property. Specifies whether list should be restarted at each section"
type: docs
weight: 50
url: /nodejs-net/aspose.words/list/isRestartAtEachSection/
---

## List.isRestartAtEachSection property

Specifies whether list should be restarted at each section.
Default value is ``false``.



```js
get isRestartAtEachSection(): boolean
```

### Remarks

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) is higher then [OoxmlCompliance.Ecma376_2006](../../../aspose.words.saving/ooxmlcompliance/#Ecma376_2006).




### Examples

Shows how to configure a list to restart numbering at each section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

doc.lists.add(aw.Lists.ListTemplate.NumberDefault);

let list = doc.lists.at(0);
list.isRestartAtEachSection = restartListAtEachSection;

// The "IsRestartAtEachSection" property will only be applicable when
// the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
let options = new aw.Saving.OoxmlSaveOptions();
options.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Transitional;

builder.listFormat.list = list;

builder.writeln("List item 1");
builder.writeln("List item 2");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.writeln("List item 3");
builder.writeln("List item 4");

doc.save(base.artifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new aw.Document(base.artifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

expect(doc.lists.at(0).isRestartAtEachSection).toEqual(restartListAtEachSection);
```

### See Also

* module [Aspose.Words](../../)
* class [List](../)

