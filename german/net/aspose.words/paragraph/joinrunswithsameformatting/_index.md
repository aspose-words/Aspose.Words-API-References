---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words für .NET
description: Verbinden Sie mühelos Läufe mit konsistenter Formatierung in Ihren Absätzen mit der Methode „JoinRunsWithSameFormatting“. Verbessern Sie noch heute den Stil Ihres Dokuments!
type: docs
weight: 300
url: /de/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

Verbindet Textläufe mit gleicher Formatierung im Absatz.

```csharp
public int JoinRunsWithSameFormatting()
```

### Rückgabewert

Anzahl der durchgeführten Verknüpfungen. Wann**N** Wenn benachbarte Läufe verbunden werden, zählen sie als**N - 1** schließt sich an.

## Beispiele

Zeigt, wie Sie Absätze durch das Zusammenführen überflüssiger Absätze vereinfachen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie vier Textzeilen in den Absatz ein.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// Wenn wir dieses Dokument in Microsoft Word öffnen, sieht der Absatz wie ein nahtloser Textkörper aus.
// Es besteht jedoch aus vier separaten Durchläufen mit der gleichen Formatierung. Fragmentierte Absätze wie dieser
// kann auftreten, wenn wir Teile eines Absatzes in Microsoft Word mehrmals manuell bearbeiten.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// Ändern Sie den Stil des letzten Laufs, um ihn von den ersten drei abzuheben.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// Wir können die Methode "JoinRunsWithSameFormatting" ausführen, um den Inhalt des Dokuments zu optimieren
// indem ähnliche Läufe zu einem zusammengeführt werden, wodurch ihre Gesamtzahl reduziert wird.
// Diese Methode gibt auch die Anzahl der Läufe zurück, die diese Methode zusammengeführt hat.
// Diese beiden Zusammenführungen erfolgten, um die Läufe Nr. 1, Nr. 2 und Nr. 3 zu kombinieren.
// wobei Lauf Nr. 4 ausgelassen wird, da er einen inkompatiblen Stil hat.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// Die Anzahl der verbleibenden Läufe entspricht der ursprünglichen Anzahl
// abzüglich der Anzahl der Run-Merges, die die Methode „JoinRunsWithSameFormatting“ durchgeführt hat.
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
