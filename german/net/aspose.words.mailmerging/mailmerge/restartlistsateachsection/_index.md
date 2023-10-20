---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words für .NET
description: MailMerge RestartListsAtEachSection eigendom. Ruft einen Wert ab oder legt diesen fest der angibt ob Listen in jedem Abschnitt nach der Ausführung eines Seriendrucks neu gestartet werden in C#.
type: docs
weight: 110
url: /de/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Ruft einen Wert ab oder legt diesen fest, der angibt, ob Listen in jedem Abschnitt nach der Ausführung eines Seriendrucks neu gestartet werden.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR` .

## Beispiele

Zeigt, wie Sie steuern können, ob die Listennummerierung in jedem Abschnitt neu gestartet wird, wenn ein Seriendruck durchgeführt wird.

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
