---
title: MailMergeSettings.activeRecord property
linktitle: activeRecord property
articleTitle: activeRecord property
second_title: Aspose.Words for NodeJs
description: "MailMergeSettings.activeRecord property. Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word"
type: docs
weight: 20
url: /nodejs-net/aspose.words.settings/mailmergesettings/activeRecord/
---

## MailMergeSettings.activeRecord property

Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1.


```js
get activeRecord(): number
```

### Examples

Shows how to execute a mail merge while connecting to an external data source.

```js
let doc = new aw.Document(base.myDir + "Odso data.docx");
let settings = doc.mailMergeSettings;

console.log(`Connection string:\n\t${settings.connectString}`);
console.log(`Mail merge docs as attachment:\n\t${settings.mailAsAttachment}`);
console.log(`Mail merge doc e-mail subject:\n\t${settings.mailSubject}`);
console.log(`Column that contains e-mail addresses:\n\t${settings.addressFieldName}`);
console.log(`Active record:\n\t${settings.activeRecord}`);

let odso = settings.odso;

console.log(`File will connect to data source located in:\n\t\"${odso.dataSource}\"`);
console.log(`Source type:\n\t${odso.dataSourceType}`);
console.log(`UDL connection string:\n\t${odso.udlConnectString}`);
console.log(`Table:\n\t${odso.tableName}`);
console.log(`Query:\n\t${doc.mailMergeSettings.query}`);

// We can reset these settings by clearing them. Once we do that and save the document,
// Microsoft Word will no longer execute a mail merge when we use it to load the document.
settings.clear();

doc.save(base.artifactsDir + "MailMerge.OdsoEmail.docx");
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [MailMergeSettings](../)

