---
title: ListCollection.AddSingleLevelList
linktitle: AddSingleLevelList
articleTitle: AddSingleLevelList
second_title: Aspose.Words für .NET
description: Erstellen und fügen Sie mit der AddSingleLevelList-Methode von ListCollection mühelos eine einstufige Liste zu Ihrem Dokument hinzu und verbessern Sie so die Organisation und Übersichtlichkeit.
type: docs
weight: 60
url: /de/net/aspose.words.lists/listcollection/addsinglelevellist/
---
## ListCollection.AddSingleLevelList method

Erstellt eine neue einstufige Liste basierend auf der vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu.

```csharp
public List AddSingleLevelList(ListTemplate listTemplate)
```

## Beispiele

Zeigt, wie eine neue einstufige Liste basierend auf der vordefinierten Vorlage erstellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ListCollection listCollection = doc.Lists;

// Erstellt die Aufzählungsliste aus der BulletCircle-Vorlage.
List bulletedList = listCollection.AddSingleLevelList(ListTemplate.BulletCircle);

// Schreibt die Aufzählungsliste in das resultierende Dokument.
builder.Writeln("Bulleted list starts below:");
builder.ListFormat.List = bulletedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Erstellt die nummerierte Liste aus der Vorlage NumberUppercaseLetterDot.
List numberedList = listCollection.AddSingleLevelList(ListTemplate.NumberUppercaseLetterDot);

// Schreibt die nummerierte Liste in das resultierende Dokument.
builder.Writeln("Numbered list starts below:");
builder.ListFormat.List = numberedList;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Save(ArtifactsDir + "Lists.AddSingleLevelList.docx");
```

### Siehe auch

* class [List](../../list/)
* enum [ListTemplate](../../listtemplate/)
* class [ListCollection](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
