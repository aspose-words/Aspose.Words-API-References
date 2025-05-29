---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMerge-Eigenschaft „RestartListsAtEachSection“ – die Kontrolllisten werden in jedem Abschnitt zurückgesetzt, um nahtlose Serienbriefe zu ermöglichen. Verbessern Sie noch heute die Präzision Ihrer Dokumente!
type: docs
weight: 110
url: /de/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Listen nach der Ausführung eines Seriendrucks in jedem Abschnitt neu gestartet werden.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt, wie gesteuert wird, ob die Listennummerierung bei jedem Abschnitt neu gestartet wird, wenn ein Seriendruck ausgeführt wird.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
